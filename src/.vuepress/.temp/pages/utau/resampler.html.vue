<template><div><div class="hint-container info">
<p class="hint-container-title">什么是引擎？</p>
<p>一般我们将Utau中的重采样器和拼接合成器称为<strong>引擎</strong>（<strong>engine</strong>），重采样器（Resampler）承载了音频的拉伸变形处理等等主要功能，而拼接合成器（Wavtool）则负责将重采样器处理过的音频进行合并。</p>
<p>如Moresampler这样的引擎同时包含了resampler和wavtool的功能，请在使用时将wavtool也指定为Moresampler。</p>
</div>
<h2 id="如何安装引擎" tabindex="-1"><a class="header-anchor" href="#如何安装引擎" aria-hidden="true">#</a> 如何安装引擎？</h2>
<p>OpenUtau会在第一次启动之后自动在安装文件夹中生成Resamplers和Wavtools文件夹。</p>
<figure><img src="https://img.kyoku.top/20231212090107.png" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>你只需要将从其他地方下载来的重采样器和合成器分别放进对应的文件夹即可，例如对于Utau的新默认引擎Doppeltler，你需要将<a href="http://utau2008.xrea.jp/2020/engine/doppeltler009.zip" target="_blank" rel="noopener noreferrer">Doppelter64.exe<ExternalLinkIcon/></a>放入Resamplers文件夹中，将<a href="http://utau2008.xrea.jp/2020/engine/wavtool64.zip" target="_blank" rel="noopener noreferrer">Wavtool64.exe<ExternalLinkIcon/></a>放入Wavtools文件夹中。</p>
<p>在将重采样器和合成器放入对应位置后，你就可以在OpenUtau中找到它们了！</p>
<p>在你需要切换引擎的轨道旁边找到引擎设置选项，选中CLASSIC引擎。</p>
<figure><img src="https://img.kyoku.top/20231212092107.png" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>然后点击旁边的小齿轮，设置重采样器和Wavtool。</p>
<figure><img src="https://img.kyoku.top/20231212095058.png" alt=" " tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<p>锵锵，你已经设置好新的引擎了！</p>
<h2 id="一些自用引擎" tabindex="-1"><a class="header-anchor" href="#一些自用引擎" aria-hidden="true">#</a> 一些自用引擎</h2>
<div class="hint-container tip">
<p class="hint-container-title">提示</p>
<p>这个部分会用来展示同一声库用不同引擎去渲染同一段工程会有什么不同。</p>
<p>默认使用的声库为Utau中华组的<a href="https://www.bilibili.com/video/BV12W411L7gA" target="_blank" rel="noopener noreferrer">氷 クカミ Tender<ExternalLinkIcon/></a>。</p>
<p><s>支持冰狼谢谢喵，冰狼宝贝可爱的喵</s></p>
<p>示例工程为<a href="https://www.bilibili.com/video/BV1t8411j7we" target="_blank" rel="noopener noreferrer">部屋に照らされた光<ExternalLinkIcon/></a>，原作にほしか，UST来自星乃スイ。</p>
<p>Pit如下：</p>
<figure><img src="https://img.kyoku.top/20231212175422.png" alt="在OpenUtau中进行了粗略的响度控制" tabindex="0" loading="lazy"><figcaption>在OpenUtau中进行了粗略的响度控制</figcaption></figure>
</div>
<details class="hint-container details"><summary>不同的引擎有有什么区别和共同点吗?</summary>
<p>Utau本身长期作为音声合成技术更新迭代的承载平台，不同引擎之间的原理相差天差地别。</p>
<p>基于其大致的合成方法，我们可以将引擎简略的分为 <strong>拼接式</strong> 和 <strong>建模式</strong> 两个大类。</p>
<p>拼接式即以fresamp为代表的一大类引擎，这类引擎运行时直接对原采样按照生成好的周波表进行处理变调和拉伸等处理。（也称非参量引擎）</p>
<p>建模式（或称参量引擎）则是以Moresampler为代表，建模式引擎会在运行时对采样进行分析并对其进行建模，完成建模后直接从其生成的模型渲染音频，这样可以实现更多变的声音处理。</p>
<p>而基于不同的合成过程，我们还可以将引擎分为 <strong>延长式</strong> 和 <strong>循环式</strong>。</p>
<p>这一区别主要在于随着音符时长增大超过了声库oto中设置的元音长度之后引擎如何继续处理。</p>
<p>对于延长式引擎，会对oto的元音部分进行分析后对其中的重复部分复制并不断拼接在一起实现延长，一般来讲，延长可以实现更自然的效果，对声库录制的要求更小，但是音质可能偏差。</p>
<p>循环式引擎会将oto的元音部分进行循环拼贴，对音质的影响很小，但是对声库录制时元音部分的稳定度要求极高，可能会产生一些很莫名其妙的问题。</p>
</details>
<h3 id="fresamp14" tabindex="-1"><a class="header-anchor" href="#fresamp14" aria-hidden="true">#</a> Fresamp14</h3>
<figure><img src="https://img.kyoku.top/fresamp14.webp" alt=" " width="80%" tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<audio controls="controls">
    <source src="https://img.kyoku.top/Fresamp14Preview_Track3.ogg" type="audio/ogg">
</audio>
<p>你可以理解为这个才是Utau一直以来事实上的官方引擎。</p>
<p>由Utau的开发者饴屋p开发的引擎，从Utau发布开始一直迭代到2013年，但是并不随Utau安装一并附带。</p>
<p><s>（附带的是效果超差的Resampler.exe）</s></p>
<p>比较有年头的引擎，中频表现尚可，高频失真明显，声噪偏大。</p>
<p><a href="http://utau2008.xrea.jp/downloads/fresamp014.zip" target="_blank" rel="noopener noreferrer">Fresamp14-饴屋p官网配布<ExternalLinkIcon/></a></p>
<p>需要配合wavtool使用，建议使用饴屋的Wavtool系列。</p>
<p><a href="http://utau2008.xrea.jp/2020/engine/wavtool64.zip" target="_blank" rel="noopener noreferrer">Wavtool64-饴屋p官网配布<ExternalLinkIcon/></a></p>
<h3 id="doppelter" tabindex="-1"><a class="header-anchor" href="#doppelter" aria-hidden="true">#</a> Doppelter</h3>
<figure><img src="https://img.kyoku.top/doppelter.webp" alt=" " width="80%" tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<audio controls="controls">
    <source src="https://img.kyoku.top/DoppelterPreview_Track3_Track3.ogg" type="audio/ogg">
</audio>
<p>同样由饴屋p开发，作为Utau的新默认引擎来开发。</p>
<p>（结果Utau编辑器本身的迭代停在了2013年，20年才发布的Doppelter至今没有等到它开箱附赠的那天，不愧是你啊Ameya。）</p>
<p>作为纯拼接式引擎，表现优秀，可以说是万金油，听感比较自然。</p>
<p><a href="http://utau2008.xrea.jp/2020/engine/doppeltler009.zip" target="_blank" rel="noopener noreferrer">Doppelter009-饴屋p官网配布<ExternalLinkIcon/></a></p>
<h3 id="moresampler" tabindex="-1"><a class="header-anchor" href="#moresampler" aria-hidden="true">#</a> Moresampler</h3>
<figure><img src="https://img.kyoku.top/moresampler.webp" alt=" " width="80%" tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<audio controls="controls">
    <source src="https://img.kyoku.top/MoresamplerPreview_Track3_Track3_Track3_Track3.ogg" type="audio/ogg">
</audio>
<p>由 Kanru Hua 开发的建模式引擎。</p>
<p>Moresampler以及其代表性的LLSM技术可以说宣告了这一代歌声合成技术探索的华丽结尾，Mores是一个近乎六边形的合成引擎，有着摸不到边的上限。</p>
<p>人声饱满清晰，细节还原度高，张力效果好，高频略少但是可以通过flag适当补足。</p>
<p>有大量独占的好用优秀flag，可以用全局flag改变音色。</p>
<p>缺点是遇到首次合成的采音时需要生成一遍llsm模型（有些声库已经自带了），速度偏慢。即便是生成过模型后合成速度也属于稍慢的一类，对低性能cpu设备压力很大。</p>
<p>比较吃录音质量，对于录音差的声库效果会不那么理想。</p>
<p>可以说是Utau框架下的引擎中渲染质量最接近商业方案（如Vocaloid）的。</p>
<p>由于Kanru Hua已经毕业，而原配布页面在其UIUC校内博客上，现已不能访问，只能提供UtaForum上的授权镜像链接。</p>
<p><a href="https://utaforum.net/threads/moresampler-0-8-4-download.19264/" target="_blank" rel="noopener noreferrer">UtaFourm<ExternalLinkIcon/></a></p>
<details class="hint-container details"><summary>关于Kanru Hua?</summary>
<p>Well，如果你有经常关注过SVS技术发展，那么你肯定会对Kanru Hua这个名字感到眼熟。</p>
<p>如果这样你还没想起来这是谁，他曾用的网名是<strong>SleepWalking</strong>，本名<strong>华侃如</strong>，现在是Synthsizer V的开发者兼创始人。</p>
<p>Moresampler的起步源自他很早以前参与的Rocaloid/RUCE项目，最初致力于让Miku可以唱出中文。</p>
<BiliBili bvid="BV1ix411F7NZ"/><p>这就是，梦开始的地方。</p>
<p>Rocaloid在项目停止之前总共进行过三次迭代，最终发布了可供Utau使用的RUCE引擎，这一引擎已经具有了建模引擎的特点，会生成.rudb模型文件，专攻中文单独音声库。</p>
<p>不久之后，SleepWalking就发布了Moresampler，这也是他探索音声合成技术的第四次迭代。</p>
<p>而Synthsizer V中的V正是罗马数字5，他一直都没有忘记一开始的那个梦想。他真的，我哭死.jpg</p>
<BiliBili bvid="BV1Yt411k7bt"/><p>实际上SynthV在早先的Std版本并没有脱离Utau的框架，SynthV的架构实质上是在Moresampler这一重采样器的技术基础上加以神经网络模型替换掉Utau框架下的Wavtool拼接合成引擎，也就是采样+AI模型的架构，在当时音声合成的AI模型技术尚未发展成熟的时候实现了极为优秀的效果。直到SynthV AI更新后才重采样引擎这一技术才算是真正成为了历史。</p>
</details>
<h3 id="worldline" tabindex="-1"><a class="header-anchor" href="#worldline" aria-hidden="true">#</a> Worldline</h3>
<figure><img src="https://img.kyoku.top/worldliner.webp" alt=" " width="80%" tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<audio controls="controls">
    <source src="https://img.kyoku.top/WorldlineRPreview_Track3_Track3_Track3.ogg" type="audio/ogg">
</audio>
<p>OpenUtau自带的极为神秘的重采样器，基于WORLD算法的建模引擎，中频表现出色，可以合成出比较扎实的人声，但是中高频分布夸张，高频有一定失真，比较依赖混音补正。</p>
<p>由于很新所以比较难找他的资料，使用尚需自己多摸索。</p>
<p>合成速度非常非常快，配合OpenUtau会让人有种在用Vocaloid的错觉（）</p>
<p>OpenUtau自带，无需下载。</p>
<h3 id="tips" tabindex="-1"><a class="header-anchor" href="#tips" aria-hidden="true">#</a> TIPS</h3>
<figure><img src="https://img.kyoku.top/tips.webp" alt=" " width="80%" tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<audio controls="controls">
    <source src="https://img.kyoku.top/TIPSPreview_Track3_Track3_Track3_Track3_Track3.ogg" type="audio/ogg">
</audio>
<p>ScientistB开发的老牌建模系重采样器，性能优秀，据说也是World算法，由于年代太久加上很多资料佚失已经难以考证了，不过听感确实非常接近world系引擎的表现。</p>
<p>合成效果比较柔和，人声中频饱满度略差于Moresampler，但是中低频表现更加优秀，比Moresampler更适合用来制作装饰效果（如怒声，气泡音等），经常和Moresampler组合使用（需要开启Moresampler的重采样器兼容）。</p>
<p><a href="http://scientistb.web.fc2.com/program/TIPS.zip" target="_blank" rel="noopener noreferrer">ScientistB官网配布<ExternalLinkIcon/></a></p>
<h3 id="tn-fnds" tabindex="-1"><a class="header-anchor" href="#tn-fnds" aria-hidden="true">#</a> tn_fnds</h3>
<figure><img src="https://img.kyoku.top/tn_fnds.webp" alt=" " width="80%" tabindex="0" loading="lazy"><figcaption> </figcaption></figure>
<audio controls="controls">
    <source src="https://img.kyoku.top/tn_fndsPreview_Track3_Track3_Track3_Track3.ogg" type="audio/ogg">
</audio>
<p>由Zteer开发，同样是基于World算法的建模系引擎，是有着独特风味的重采样器，人声沙哑有一点底噪，但是模糊的恰到好处，很适合一些感情色调明显的歌曲。</p>
<p><a href="http://z-server.game.coocan.jp/utau/tn_fnds009.zip" target="_blank" rel="noopener noreferrer">Zteer官网配布<ExternalLinkIcon/></a></p>
</div></template>


