# mousesheel
鼠标滚轮事件
<pre>
    document.onmousewheel=wheel;
    if(document.addEventListener) document.addEventListener('DOMMouseScroll',wheel,false);  //Firefox 专用事件DOMMouseScroll
    function wheel(event){
        var e=event || window.event;
        if(e.wheelDelta){
            if(e.wheelDelta>0){  //鼠标往上 滚动 wheelDelta的值等于 120
                alert('上')
            }else{                //鼠标往下 滚动 wheelDelta的值等于 -120
                alert('下')
            }
        }else if(e.detail){  //Firefox的属性是detail       Firefox正负和其他浏览器相反
            if(e.detail<0){  //Firefox下鼠标往上 滚动 detail的值等于 -3
                alert('Firefox 上')
            }else{           //Firefox下鼠标往下 滚动 detail的值等于 3
                alert('Firefox 下')
            }
        }
    }
</pre>
