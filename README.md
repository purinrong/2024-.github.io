<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
          margin: 0;
          padding: 0;
          background-image: url(算命狗狗.png);
          background-size: 720px 720px;
          background-position: center;
          background-attachment: fixed;
          background-repeat: no-repeat;
        }
        header {
            text-align: center;
            padding: 50px;
        }

        main {
            text-align: center;
            padding: 20px;
        }

        footer {
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        div{
            font-size: 30px;
            font-weight: bold;
            color: #664f4b;
            font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            /*text-align: center;*/
        }
    </style>
</head>
<body>
    <div id="ready1" style="position: absolute; top: 152px; left:470px;"> </div>
    <div id="ready2" style="position: absolute; top: 248px; left:470px;"> </div>
    <div id="ready3" style="position: absolute; top: 342px; left:470px;"> </div>
    <div id="start" style="cursor: pointer; position: absolute; " onclick="doit()">開始算命</div>

    <script>
        var names1=["成為水餃皮的粉絲","升職","長高五公分","瘋狂豔遇","出國三次","被詐騙","不會被詐騙","改掉一個壞習慣","身體健康"
        ,"完成一個大項目","學會一個新技能","長高十公分","瘦五公斤","成為炸雞狗的信徒","獲得一百萬","中樂透/發票","財富自由"
        ,"吃不胖","電子產品都不會壞","投資成功"]

        var names2=["桃花超旺","找到男/女朋友","成為網紅","獲得超能力","早睡早起",
        "皮膚變好","不會便秘","大家都會聽你的意見","交換禮物不會換到垃圾","出去玩都是好天氣"
        ,"規律運動","買東西不踩雷","養一隻貓","養一隻狗","換新髮型不會被笑","分組不會遇到雷包"
        ,"房間一整年都很乾淨","家裡不會出現蟑螂","每天都很開心","每天看一本書"]

        var names3=["找到之前弄丟的東西","每天都睡很飽","看電影不會被爆雷","不會遇到破人破事","遇見喜歡的明星"
        ,"不會糾結要吃什麼","喜歡的插畫家出新貼圖","想買的東西剛好打折","去算命不會被谝","白色的衣服不會弄髒","變成一顆馬鈴薯"
        ,"判斷力變好","走出舒適圈","扛壓力變好","出門被叫帥哥/美女","學會一種新樂器","寫程式沒有bug"
        ,"參加三場演唱會","有一棟自己的房子","變成團寵"]   
        var time=null;
        function doit(){
            var button=window.document.getElementById("start"); 
                if(time==null){
                    button.innerHTML="確認命運";
                    show();
                }else{
                    button.innerHTML="開始算命";
            clearInterval(time);
            time=null;
                }

        }
        function show(){
            var box1=window.document.getElementById("ready1");
            var box2=window.document.getElementById("ready2");
            var box3=window.document.getElementById("ready3");
            var num1=Math.floor(Math.random()*100000)%names1.length;
            var num2=Math.floor(Math.random()*100000)%names2.length;
            var num3=Math.floor(Math.random()*100000)%names3.length;
            box1.innerHTML=names1[num1];
            box2.innerHTML=names2[num2];
            box3.innerHTML=names3[num3];
            time=setTimeout("show()",1);}
/*----------------------------------------------------------------------------------------*/
    </script>

</body>
</html>
