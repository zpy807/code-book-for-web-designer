第十三章 相对地址
===

到这里我们必须先说清楚一个概念：相对地址。以后涉及到文件的地方我们要经常用到这个概念，所以还是先讲清楚了的好。

地址是用来描述描述文件位置的，它分为绝对地址和相对地址。

绝对地址：比如 C:\windows\，再比如 http://www.google.com ，这样拿出来就能确切制定一个位置，不会产生任何疑问的地址就是绝对地址。

相对地址，有了相对两个字就得有个参照物，你距离我 100 米，我就是参照物，没有我这个参照物，100 米这个距离就没有任何意义。在我们说相对地址的时候一般的是在那里说就以哪里为参照物。在 a.html 这个文件里的相对地址就以 a.html 这个文件作为参照物。

现在开始举例子时间，我们假设我们有如下的目录结构，没有后缀的就是文件夹，

	MyCode
		index.html
		images
			pic.jpg
			1.html
		css
			style.css
		haha.jpg

这个结构我希望大家能够看懂，MyCode 是我们存放这些文件的文件夹，里边有 images 和 css 两个文件夹，还有 index.html 和 haha.jpg 两个文件，然后 那两个文件夹里还有……文件。

现在我们在 index.html 里写其他几个文件的相对地址

	images/pic.jpg
	images/1.html
	css/style.css
	haha.jpg

然后自己理解一下，那么我们在 index.html 文件里写一个显示图片的代码就可以写作

	<img src="images/pic.jpg" />

现在我们好像开始理解相对地址了呢，那就换个角度看问题，在 1.html 里些其他文件的相对地址会是怎么样的？

	../index.html
	pic.jpg
	../css/style.css
	../haha.jpg

.. 代表的就是上一层文件夹了。那要是上两层文件夹呢？../../ 这样啊。好像相对地址也没多复杂。那在 style.css 里怎么写呢？

	../index.html
	../images/pic.jpg
	../images/1.html
	../haha.jpg