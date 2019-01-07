# Test


* 以下内容不可用在文档内
		<script language='javascript' type='text/javascript'>
		function delayShow(start)
		    {
				alert("test")
		        /**
		        *1.delay函数是jquery 1.4.2新增的函数
		        *2.hide函数里必须放一个0,不然延时不起作用
		        */
		        //$('#divid').delay(6000).hide(0);
				if(start==0){
					document.getElementById('testButton').disabled="enabled";
					document.getElementById('testButton').value="Click Me!";
					return;
				}
				document.getElementById('testButton').value=start+"Click Me!";
				t=setTimeout('delayShow(start-1)',500);
		    }

		</script>


		<body onload="delayShow(10)">
		<input type="button" disabled="disabled" id="testButton" name="testButton" value=""/>
		</body>