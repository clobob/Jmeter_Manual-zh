# BeanShell 概述

> BeanShellSampler 

用户可以使用BeanShell脚本语言自定义采样器. BeanShell 语法请参照 [BeanShell website](http://www.beanshell.org) .测试元素支持 **ThreadListener** 与 **TestListener** 的接口方法, 这些方法需要被预定义在初始化文件中. 定义举例：
<details>
<summary>BeanShellListener.bshrc (Click to expand)</summary>
	
	// Example BeanShell Listener definitions
	
	// ThreadListener methods

	threadStarted(){
		print("threadStarted");
	}

	threadFinished(){
		print("threadFinished");
	}

	// TestListener methods

	testStarted(){
		print("testStarted");
	}

	testEnded(){
		print("testEnded");
	}

	testStarted(String s){
		print("testStarted "+s);
	}

	testEnded(String s){
		print("testEnded "+s);
	}
</details>	

BeanShell 还支持 **Interrruptible** 接口, 方法 _interrupt()_ 可以被定义在脚本中或者初始文件中。
