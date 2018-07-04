<template>
  <div class="layui-body">
    <!-- 内容主体区域 -->
    <div style="padding: 15px;">
        <div class="site-title">
		      <fieldset><legend><a name="fieldset" >人员清单</a></legend></fieldset>
		    </div>
		    <div class="table-model1">
		    	 <table id="person" lay-filter="test"></table>
		    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  created:function(){
    //JavaScript代码区域
    layui.use('element', function(){
      var element = layui.element;
    });
    layui.use('table', function(){
     var table = layui.table;
      //第一个实例
		 table.render({
		    elem: '#person'
		    ,height: 315
		    ,url: '' //数据接口
		    ,page: true //开启分页
		    ,data:[
		      {"id":'10001','username':'user-01','sex':'男','city':'北京','sign':'签名1','experience':'1000','score':'90','classify':'老师','wealth':'100000' },
		      {"id":'10002','username':'小树','sex':'男','city':'武汉','sign':'签名1','experience':'1000','score':'59','classify':'央企','wealth':'100000' },
		      {"id":'10003','username':'召唤师','sex':'男','city':'深圳','sign':'签名1','experience':'1000','score':'80','classify':'EE','wealth':'100000' },
		      {"id":'10004','username':'kaka','sex':'男','city':'深圳','sign':'签名1','experience':'1000','score':'80','classify':'JAVA','wealth':'100000' },
		      {"id":'10005','username':'盼盼','sex':'男','city':'深圳','sign':'签名1','experience':'1000','score':'80','classify':'前端','wealth':'100000' } 
		     ]
		    ,cols: [[ //表头
		      {field: 'id', title: 'ID', width:'10%', sort: true, fixed: 'left'}
		      ,{field: 'username', title: '用户名', width:'10%'}
		      ,{field: 'sex', title: '性别', width:'10%', sort: true}
		      ,{field: 'city', title: '城市', width:'10%'} 
		      ,{field: 'sign', title: '签名', width: '10%'}
		      ,{field: 'experience', title: '积分', width: '10%', sort: true}
		      ,{field: 'score', title: '评分', width: '10%', sort: true}
		      ,{field: 'classify', title: '职业', width: '10%'}
		      ,{field: 'wealth', title: '财富', width: '20%', sort: true}
		    ]]
		  });
    });
  }
}
</script>

<style>
	.site-title{ margin: 30px 0 20px;}
	.site-title fieldset{border: none; padding: 0; border-top: 1px solid #00F7DE;}
	.site-title fieldset legend{margin-left: 20px;  padding: 0 10px; font-size: 22px; font-weight: 300;}
</style>
