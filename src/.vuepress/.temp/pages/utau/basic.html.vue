<template><div><p>在上个章节中我们已经完成了OpenUtau的基本配置，现在是时候让我们来解决<mark>主播我的Utau为什么发不出声的问题了</mark>（误</p>
<h2 id="主界面" tabindex="-1"><a class="header-anchor" href="#主界面" aria-hidden="true">#</a> 主界面</h2>
<div class="hint-container tip">
<p class="hint-container-title">提示</p>
<p><span class="xingmu"><strong>详细介绍注意！！！</strong></span></p>
<p>这里会介绍主界面的各个元素的作用，虽然个人来讲比较建议你都了解一下再上手，但是如果你觉得你完全看一眼就知道这些要怎么用，那你完全可以直接跳到下面的<a href="#%E5%BC%80%E5%A7%8B%E8%B0%83%E5%A3%B0">开始调声</a>部分。</p>
<p><s>毕竟这个部分确实稍微有些长</s></p>
</div>
<p>在打开OpenUtau后，首先进入的页面。</p>
<figure><img src="https://img.kyoku.top/mainwindow.webp" alt="主界面" tabindex="0" loading="lazy"><figcaption>主界面</figcaption></figure>
<h3 id="顶栏" tabindex="-1"><a class="header-anchor" href="#顶栏" aria-hidden="true">#</a> 顶栏</h3>
<p>我们首先从顶栏开始介绍。</p>
<figure><img src="https://img.kyoku.top/navbar.gif" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p><strong>顶栏</strong>主要承载了一些文件相关的操作以及和软件本身有关的操作。</p>
<p>点选 <strong>文件 --&gt; 新建</strong> 即可新建一个空白工程。</p>
<p>除了常用的新建、打开、保存等文件操作以外，工程、音频以及midi文件的导入导出也在这里完成。</p>
<p>作为示例，如果你需要导入多个ust工程到多个轨道上，你应该点击 <strong>文件 --&gt; 导入轨道</strong> ，然后在打开的新窗口中选中<strong>所有</strong>你需要的ust工程。</p>
<figure><img src="https://img.kyoku.top/utau-inputust.webp" alt="如图所示" tabindex="0" loading="lazy"><figcaption>如图所示</figcaption></figure>
<p>点击打开后，音轨会被加入到工程的最下方。</p>
<figure><img src="https://img.kyoku.top/afterputin.webp" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p><strong>工具</strong>选项卡中包含了一些比较常用的功能，如<strong>自动排列窗口</strong>。</p>
<figure><img src="https://img.kyoku.top/ypailie.webp" alt="这是垂直1:3排列后的效果，OpenUtau会在排列时自动设置全屏如果你比较习惯VOCALOID的界面排列方式那么这个可能会很适合你" tabindex="0" loading="lazy"><figcaption>这是垂直1:3排列后的效果，OpenUtau会在排列时自动设置全屏<br>如果你比较习惯VOCALOID的界面排列方式那么这个可能会很适合你</figcaption></figure>
<p><strong>清除缓存功能</strong>会把OpenUtau产生的所有合成缓存都删除掉，这有助于减少存储的占用并且有时候可能可以解决一些合成音频失败的问题（这个缓存不包含Moresampler和TIPS等建模类引擎生成的模型文件，请放心使用）。</p>
<p>另外，值得一提的是，OpenUtau自带了<strong>歌手管理</strong>工具，通过 <strong>工具 --&gt; 歌手</strong> 即可打开。</p>
<figure><img src="https://img.kyoku.top/singers.webp" alt="如果你折腾过声库的oto，那么你大概马上就理解这个小工具可以用来做什么了" tabindex="0" loading="lazy"><figcaption>如果你折腾过声库的oto，那么你大概马上就理解这个小工具可以用来做什么了</figcaption></figure>
<p><s>当然如果你只是刚刚打算入门的萌新那么你也可以看过了事，以后也许也会有看懂并且用到这里的东西的一天的XD</s></p>
<h3 id="控件栏" tabindex="-1"><a class="header-anchor" href="#控件栏" aria-hidden="true">#</a> 控件栏</h3>
<figure><img src="https://img.kyoku.top/speed.webp" alt="左边用于设置曲速和节拍 中间用来控制预览播放 右边则显示播放标记的时间位置" tabindex="0" loading="lazy"><figcaption>左边用于设置曲速和节拍 中间用来控制预览播放 右边则显示播放标记的时间位置</figcaption></figure>
<p>可以在这个控件栏中设置工程的<strong>曲速</strong>和<strong>节拍</strong>（当然也可以在右边的音轨器中设置曲速和节拍标记）</p>
<div class="hint-container info">
<p class="hint-container-title">曲速和节拍</p>
<p><strong>BPM</strong>即Beats Per Minutes，每分钟节拍数</p>
<p>工程的BPM一般和你的乐曲的BPM设置成<strong>相同</strong>或者倍数关系。</p>
<p>而<strong>节拍</strong>则是指工程的每小节有几拍（4/4即每小节4拍，每个音符的单位为四分之一拍）</p>
<p>如果你不知道你需要调声的音频的BPM，你可以使用这个工具进行测量 --&gt; <a href="https://vocalremover.org/zh/key-bpm-finder" target="_blank" rel="noopener noreferrer">Vocalremover<ExternalLinkIcon/></a></p>
<p>这个工具网页也可以用来给提取音频中的干声和伴奏，建议收藏~</p>
</div>
<h3 id="侧边栏-音轨管理" tabindex="-1"><a class="header-anchor" href="#侧边栏-音轨管理" aria-hidden="true">#</a> 侧边栏（音轨管理）</h3>
<figure><img src="https://img.kyoku.top/track_manager.webp" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>侧栏主要显示对应音轨上的<strong>声库信息</strong>，包括最左侧的声库头图、音轨名、选用的声库、使用的声码器、引擎设置、音量滑条及播放控制。</p>
<p>在侧栏中<strong>点击声库名称</strong>即可展开声库列表，可以在这里选择切换你已经安装过的声库。</p>
<div class="hint-container note">
<p class="hint-container-title">注</p>
<p>如果你现在就想开始安装声库，可以跳到<a href="#%E5%AE%89%E8%A3%85%E5%A3%B0%E5%BA%93">#安装声库</a></p>
</div>
<figure><img src="https://img.kyoku.top/../.vuepress/public/choose_singer.gif" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p><strong>点击声码器名称</strong>即可展开声码器列表（默认为DEFAULT，会自动根据声库设置切换声码器，如果你发现默认的声码器没有办法正常渲染声音可以在这里切换声码器。）</p>
<figure><img src="https://img.kyoku.top/vocalencoder.gif" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<div class="hint-container info">
<p class="hint-container-title">声码器的选择</p>
<p>不同的声码器接受的音符名称格式和音源是不一样的，一般推荐对日语VCV和CVVC声库使用这里的 <u>JA VCV&amp;CVVC</u> 声码器，这个声码器可以同时接受输入あえいおうアエイオウ这样的假名，也可以输入aeiou这样的罗马音，可以有效防止<mark>发不出声</mark>这个问题的出现XD</p>
</div>
<figure><img src="https://img.kyoku.top/aeiou.webp" alt="使用 VCV&amp;CVVC 声码器时输入あえいおう和aeiou是完全等价的" tabindex="0" loading="lazy"><figcaption>使用 VCV&amp;CVVC 声码器时输入あえいおう和aeiou是<strong>完全等价</strong>的</figcaption></figure>
<p><strong>点击引擎分类</strong>可以切换内置的<strong>WORLDLINE-R引擎</strong>和<strong>CLASSIC引擎</strong>（即<u>和Utau相同的基于重采样器和合成器的构造的引擎组合</u>）而右边的小齿轮可以打开当前引擎的引擎设置界面。</p>
<div class="hint-container note">
<p class="hint-container-title">注</p>
<p>如果使用WORLDLINE-R引擎那么小齿轮里应该不会有任何可配置项。</p>
<p>而使用CLASSIC引擎（如Moresampler，TIPS，doppeltler64等Utau引擎）时需要在这里配置重采样器和合成器，详见<a href="/utau/resampler">引擎设置</a></p>
</div>
<p>下面的两个小滑条分别是<strong>音量滑条</strong>和<strong>声像滑条</strong>，前者可以调整预览的音量大小（不影响单独输出的音频的音量大小，但是使用OpenUtau自带的混缩功能则会生效），而声像滑条可以调整声音的声像（即<strong>左右声道位置</strong>，往左拉满会使声像出现在左侧90度直角方位，另一侧同理）</p>
<p>右侧的M和S按钮分别表示<strong>Mute（静音）<strong>和</strong>Solo（独奏）</strong><s>真的不是SM</s>，分别会使这个轨道消音以及只播放这个轨道。（被设置静音的声轨即使单独输出音频也不会被输出，请注意）</p>
<h3 id="播放界面" tabindex="-1"><a class="header-anchor" href="#播放界面" aria-hidden="true">#</a> 播放界面</h3>
<figure><img src="https://img.kyoku.top/play.gif" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>右侧的窗口就是OpenUtau的播放界面，会显示每个声轨的音符预览，<strong>播放标记</strong>和<strong>小节号</strong>会显示在顶部，同时在顶部的最左侧会显示这个工程的<strong>默认曲速</strong>和<strong>拍号设置</strong>。</p>
<div class="hint-container note">
<p class="hint-container-title">注</p>
<p>因为实际上来讲，给工程设置bpm和拍号时其实就是直接在工程的最开头加了个bpm和拍号标记。</p>
<p>你也可以手动在顶侧右键添加拍号和bpm标记，这样可以完成一些歌曲<strong>变速</strong>的操作。</p>
</div>
<h2 id="安装声库" tabindex="-1"><a class="header-anchor" href="#安装声库" aria-hidden="true">#</a> 安装声库</h2>
<p>OpenUtau有很多种安装声库的方法，你可以直接像Utau一样解压到Singers安装声库（但是这样就会容易<u>像Utau一样产生<strong>编码问题</strong></u>，虽然你也可以直接在OpenUtau的歌手设置里<strong>修改编码格式</strong>来解决，但是终究是不够方便）</p>
<p>对于OpenUtau，我们更推荐使用<strong>拖放</strong>的方法安装，你只需要把声库（.zip, .uar, .rar, etc.）直接拖放到OpenUtau的页面中就会自动启动安装程序。</p>
<figure><img src="https://img.kyoku.top/install_bank.gif" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>在通过这种方法安装声库时，你可以设置声库的oto和配置文件的编码格式，使其可以被正确显示，然后OpenUtau会自动对声库进行转码，可以有效解决乱码和不识别的问题。</p>
<p>你也可以在 <strong>工具 --&gt; 安装歌手</strong> 里直接选中声库文件来进行安装，步骤同上。</p>
<div class="hint-container info">
<p class="hint-container-title">Utau缘何产生编码问题？</p>
<p>由于Utau诞生于上个互联网时代（2009年）并且使用Virtual Basic语言编写，它<strong>完全没有</strong>为不同的编码环境做设计（那个时代的私人共享软件传播一般不会直接考虑到这种世界范围的分发。）而日本的计算机和其他区域不同，全部使用日本规定的<strong>Shift-JIS</strong>编码（国内现在的计算机环境一般是把GB2312编码成UTF8，所以大部分情况下不会出现这么严重的编码问题。），导致在非日本地区的计算机上会产生大量的乱码错误。</p>
<p>所以解决编码问题的关键主要在于把Utau放入一个Shift-JIS的环境或者直接把Utau的字符替换成UTF-8的编码，这也是前些年主要的解决方案。</p>
<p>当然OpenUtau直接就是为了现代计算机设计的，自然也没有这个问题，但是仍然需要为各种各样的声库准备转码功能。</p>
</div>
<h2 id="开始调声" tabindex="-1"><a class="header-anchor" href="#开始调声" aria-hidden="true">#</a> 开始调声</h2>
<p>还是让我们先回到主界面里，点击右侧音轨页面即可创建新的Part。</p>
<figure><img src="https://img.kyoku.top/动画1.gif" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>双击Part即可打开编辑窗口。</p>
<figure><img src="https://img.kyoku.top/20231205090440.png" alt="如果你有过使用Cubase/FL Studio等DAW软件的经验，你应该能发现这个编辑界面其实就是钢琴窗" tabindex="0" loading="lazy"><figcaption>如果你有过使用Cubase/FL Studio等DAW软件的经验，你应该能发现这个编辑界面其实就是钢琴窗</figcaption></figure>
<p>OpenUtau的编辑界面分为顶栏（功能栏）、音符编辑（钢琴窗）以及底栏（参数编辑器）三个部分。</p>
<h3 id="编辑音符" tabindex="-1"><a class="header-anchor" href="#编辑音符" aria-hidden="true">#</a> 编辑音符</h3>
<p>OpenUtau的音符编辑器是一个典型的钢琴窗界面，它可以上下滚动，并且在最左侧标识了对应的音高。</p>
<p>在你进入这个界面时，OpenUtau会自动切换到绘制模式，你可以在钢琴窗的任一空白部分点击并拖动来创建音符，创建好的音符双击即可编辑歌词。</p>
<figure><img src="https://img.kyoku.top/动画2.gif" alt="功能栏上选项为小铅笔图标时即为绘制模式，具体会在后续章节讲解" tabindex="0" loading="lazy"><figcaption>功能栏上选项为小铅笔图标时即为绘制模式，具体会在后续章节讲解</figcaption></figure>
<p>作为示例，我们可以尝试着画一点简单的旋律。</p>
<div class="hint-container info">
<p class="hint-container-title">相关信息</p>
<p>本篇教程中，后续的操作教学都会以</p>
</div>
</div></template>


