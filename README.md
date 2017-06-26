ISDB向けlibass
=============

ISDB-S/Tで用いられる字幕を表示するため、
[ISDB向けFFmpeg](https://github.com/0p1pp1/ffmpeg)によって
取り出し・デコードされた拡張ASS形式の字幕データを描画する。

[ISDB向けmpv](https://github.com/0p1pp1/mpv)で
(ISDB向けffmpegと共に)使用されている。

## 本家からの変更点

libass 0.13.7をベースに以下の拡張・変更を加えた。

* 縦書き機能の拡張： これまでのように後で入力側で90度回転させる必要なく直接縦書きする。
* 字幕背景の追加
* 行間隔のスタイルオーバーライドの追加
* スクロールの自動停止(スライドイン)の追加
* その他本家libassでの不具合修正

## フォントについて

ISDB-S/Tの独自文字を表示する場合、それらの文字をサポートしたフォントが必要。
和田研中丸ゴシックやIPAexGothicARIB等。
ただし、これらの文字はEPGでは使用されるが字幕で使用されることは少ない。


以下、オリジナルのREADME.md

------
[![Build status](https://api.travis-ci.org/libass/libass.png)](https://travis-ci.org/libass/libass)

[![Coverity scan build status](https://scan.coverity.com/projects/3531/badge.svg)](https://scan.coverity.com/projects/3531)

libass
======
libass is a portable subtitle renderer for the ASS/SSA (Advanced Substation Alpha/Substation Alpha) subtitle format. It is mostly compatible with VSFilter.

Get it
======
See [GitHub releases](https://github.com/libass/libass/releases) for the latest release 0.13.7 (released 2017-06-03). This is mainly a security and bug fix release. See the [changelog](https://github.com/libass/libass/blob/master/Changelog) for a detailed list of changes.

Source code is available from our [GitHub repository](https://github.com/libass/libass).

Contact
=======
Please use the [issue tracker](https://github.com/libass/libass/issues?state=open) to report bugs or feature requests. We have an IRC channel, too. Talk to us on [irc.freenode.net/#libass](irc://irc.freenode.net/libass).

Related Links
=============
The following projects/companies use libass:

- [MPlayer](http://www.mplayerhq.hu/)
- [mplayer2](http://www.mplayer2.org/)
- [mpv](http://mpv.io/)
- [VLC](http://www.videolan.org/)
- [GStreamer](http://gstreamer.freedesktop.org/) (assrender plugin)
- [Libav](http://libav.org/)
- [FFmpeg](http://ffmpeg.org/)
- [Aegisub](http://www.aegisub.org/)
- [Kodi (XBMC)](http://kodi.tv/)
- [avidemux](http://fixounet.free.fr/avidemux/)
- [PunkGraphicsStream (BD subtitle encoder)](http://code.google.com/p/punkgraphicstream/)
- [HandBrake](http://handbrake.fr/)
- [Crunchyroll](http://www.crunchyroll.com/)
- [MX Player](https://play.google.com/store/apps/details?id=com.mxtech.videoplayer.ad)
- [QMPlay2](http://zaps166.sourceforge.net/?app=QMPlay2)

Information about the ASS format:
=================================
- [ASS specification (incomplete)](http://moodub.free.fr/video/ass-specs.doc)
- [ASS override tags (Aegisub manual)](http://docs.aegisub.org/latest/ASS_Tags/)
- [VSFilter source code (Guliverkli2)](http://sourceforge.net/p/guliverkli2/code/HEAD/tree/src/subtitles/)

Other ASS/SSA implementations:
==============================
- VSFilter:
  - [xy-VSFilter/XySubFilter](https://code.google.com/p/xy-vsfilter/)
  - VSFilter in [MPC-HC](http://mpc-hc.org/)
  - [VSFilterMod](https://code.google.com/p/vsfiltermod/) (with custom format extensions)
  - [Threaded VSFilter](https://code.google.com/p/threaded-vsfilter/) (defunct)
  - VSFilter in [Guliverkli2](http://sourceforge.net/projects/guliverkli2/) (defunct, subsumed by all of the above)
  - VSFilter in [guliverkli](http://sourceforge.net/projects/guliverkli/) (defunct, forked as Guliverkli2)
- [ffdshow](http://ffdshow-tryout.sourceforge.net/)
- [Perian](https://github.com/MaddTheSane/perian)
- [asa](http://git.spaceboyz.net/asa.git) (defunct)
- [libjass](https://github.com/Arnavion/libjass)
