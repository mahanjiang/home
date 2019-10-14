
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, minimum-scale=1.0, maximum-scale=1.0">
    <title>html5 canvas制作圆形水波进度条动画特效</title>

    <link href="/static/css/demo.css" rel="stylesheet" media="all" />

    <!--[if IE]>

    <style type="text/css">
        li.remove_frame a {
            padding-top: 5px;
            background-position: 0px -3px;
        }
    </style>

    <![endif]-->

    <script type="text/javascript" src="/static/js/jquery.min.js"></script>
    <script type="text/javascript" src="/static/js/jquery.qrcode.min.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {
            function fixHeight() {
                var headerHeight = $("#switcher").height();
                $("#iframe").attr("height", $(window).height()-54+ "px");
            }
            $(window).resize(function () {
                fixHeight();
            }).resize();

            $('.icon-monitor').addClass('active');

            $(".icon-mobile-3").click(function () {
                $("#by").css("overflow-y", "auto");
                $('#iframe-wrap').removeClass().addClass('mobile-width-3');
                $('.icon-tablet,.icon-mobile-1,.icon-monitor,.icon-mobile-2,.icon-mobile-3').removeClass('active');
                $(this).addClass('active');
                return false;
            });

            $(".icon-mobile-2").click(function () {
                $("#by").css("overflow-y", "auto");
                $('#iframe-wrap').removeClass().addClass('mobile-width-2');
                $('.icon-tablet,.icon-mobile-1,.icon-monitor,.icon-mobile-2,.icon-mobile-3').removeClass('active');
                $(this).addClass('active');
                return false;
            });

            $(".icon-mobile-1").click(function () {
                $("#by").css("overflow-y", "auto");
                $('#iframe-wrap').removeClass().addClass('mobile-width');
                $('.icon-tablet,.icon-mobile,.icon-monitor,.icon-mobile-2,.icon-mobile-3').removeClass('active');
                $(this).addClass('active');
                return false;
            });

            $(".icon-tablet").click(function () {
                $("#by").css("overflow-y", "auto");
                $('#iframe-wrap').removeClass().addClass('tablet-width');
                $('.icon-tablet,.icon-mobile-1,.icon-monitor,.icon-mobile-2,.icon-mobile-3').removeClass('active');
                $(this).addClass('active');
                return false;
            });

            $(".icon-monitor").click(function () {
                $("#by").css("overflow-y", "hidden");
                $('#iframe-wrap').removeClass().addClass('full-width');
                $('.icon-tablet,.icon-mobile-1,.icon-monitor,.icon-mobile-2,.icon-mobile-3').removeClass('active');
                $(this).addClass('active');
                return false;
            });
        });
    </script>

    <script type="text/javascript">
	function Responsive($a) {
		if ($a == true) $("#Device").css("opacity", "100");
		if ($a == false) $("#Device").css("opacity", "0");
		$('#iframe-wrap').removeClass().addClass('full-width');
		$('.icon-tablet,.icon-mobile-1,.icon-monitor,.icon-mobile-2,.icon-mobile-3').removeClass('active');
		$(this).addClass('active');
		return false;
	};
    </script>
	
	<script type="text/javascript" src="/static/js/protect.js"></script>
	
</head>
<body id="by">

<div id="switcher">
    <div class="center">
        <ul>
            <div id="Device">
                <li class="device-monitor"><a href="javascript:"><div class="icon-monitor"></div></a></li>
                <li class="device-mobile"><a href="javascript:"><div class="icon-tablet"></div></a></li>
                <li class="device-mobile"><a href="javascript:"><div class="icon-mobile-1"></div></a></li>
                <li class="device-mobile-2"><a href="javascript:"><div class="icon-mobile-2"></div></a></li>
                <li class="device-mobile-3"><a href="javascript:"><div class="icon-mobile-3"></div></a></li>
            </div>
            <li class="top2">
                <a href="#">手机二维码预览</a>
                <div class="vm">
                    <div id="output"></div>
                    <p style="color:#808080;margin:10px 0 0 0;">扫一扫，直接在手机上打开</p>
                </div>
            </li>
            <li class="logoTop">
                <a href="https://www.17sucai.com/pins/24471.html">html5 canvas制作圆形水波进度条动画特效</a>            <script type="text/javascript">
                jQuery('#output').qrcode({width:150,height: 150,text: window.location.href});
            </script>
            <li class="remove_frame"><a href="https://www.17sucai.com/preview/632114/2017-05-09/index/index.html" title="移除框架"></a></li>
        </ul>
    </div>
</div>

<div id="iframe-wrap">
    <iframe id="iframe" src="https://www.17sucai.com/preview/632114/2017-05-09/index/index.html" frameborder="0"  width="100%"></iframe>
</div>

<!--百度流量统计代码-->
<script>
    var _hmt = _hmt || [];
    (function() {
        var hm = document.createElement("script");
        hm.src = "https://hm.baidu.com/hm.js?382f81c966395258f239157654081890";
        var s = document.getElementsByTagName("script")[0];
        s.parentNode.insertBefore(hm, s);
    })();
</script>

</body>
</html>
