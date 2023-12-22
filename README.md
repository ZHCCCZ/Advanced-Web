<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0, shrink-to-fit=no, viewport-fit=cover">
    <title>23201012014-赵春泽</title>
    <script src="../fonts/iconfont.js"></script>
    <script src="../json/index.json"></script>
    <link rel="stylesheet" href="../css/index.css">
    <link rel="stylesheet" href="../swiper/swiper-bundle.min.css">
    <!-- 搜索框输入内容返回内容 -->
    <script>  
        function handleSearch() {  
          var input = document.getElementById('search_input').value;  
          alert("您是不是在搜索" + input + "?");  
        }  
    </script> 
</head>
<body>
    <!-- 顶部导航栏 -->
    <nav class="t_nav" id="fixed">
        <input type="search" class="search_input" id="search_input" name="search_input" placeholder="WELCOME TO STEAM STORE" onkeypress="if (event.key === 'Enter') handleSearch()"> 
        <svg class="search_input_icon" aria-hidden="true"><use xlink:href="#icon-sousuo"></use></svg>
        <div><img class="head_img" src="../image/user-head.gif"></div>
        <ul>
            <li><a href="#">菜单</a></li>
            <li><a href="#">愿望单</a></li>
            <li><a href="#">钱包</a></li>
        </ul>
    </nav>
    <!-- 底部导航栏 -->
    <nav class="b_nav">
        <ul>
            <li><a href="./index.html"><svg class="b_nav_icon" aria-hidden="true"><use xlink:href="#icon-biaoqian-copy"></use></svg></a></li>
            <li><a href="./new.html"><svg class="b_nav_icon" aria-hidden="true"><use xlink:href="#icon-xinwen09"></use></svg></a></li>
            <li><a href="./safe.html"><svg class="b_nav_icon" aria-hidden="true"><use xlink:href="#icon-yangshi_icon_tongyong_shield"></use></svg></a></li>
            <li><a href="./note.html"><svg class="b_nav_icon" aria-hidden="true"><use xlink:href="#icon-icons_notifications"></use></svg></a></li>
            <li><a href="./user.html"><svg class="b_nav_icon" aria-hidden="true"><use xlink:href="#icon-liebiaogengduo-More"></use></svg></a></li>
        </ul>
    </nav>
    <!-- 内容 -->
    <a href="https://store.steampowered.com/"><div class="advert_background"></div></a>
    <h1 class="concent-title">精选和推荐</h1>
    <div class="swiper mySwiper">
        <div class="swiper-wrapper">
            <div class="swiper-slide"><img src="../image/capsule_1.jpg"><div class="swiper-slide-des">Counter-Strike 2<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_2.jpg"><div class="swiper-slide-des">房产达人 2<div class="swiper-slide-price">HK$ 175.50</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_3.jpg"><div class="swiper-slide-des">Monster Hunter: World<div class="swiper-slide-price">HK$ 77.22</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_4.jpg"><div class="swiper-slide-des">使命召唤®<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_5.jpg"><div class="swiper-slide-des"> PUBG: BATTLEGROUNDS<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_6.jpg"><div class="swiper-slide-des"> Apex Legends™<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_7.jpg"><div class="swiper-slide-des"> World of Warships<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_8.jpg"><div class="swiper-slide-des"> Granblue Fantasy Versus: Rising<div class="swiper-slide-price">HK$ 398.00</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_9.jpg"><div class="swiper-slide-des"> Warframe<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_10.jpg"><div class="swiper-slide-des"> 战意<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_11.jpg"><div class="swiper-slide-des">THE FINALS<div class="swiper-slide-price">免费开玩</div></div></div>
            <div class="swiper-slide"><img src="../image/capsule_12.jpg"><div class="swiper-slide-des">魔法使之夜<div class="swiper-slide-price">HK$ 328.50</div></div></div>
        </div>
        <div class="swiper-scrollbar"></div>
    </div>
    <div class="tab">
        <div class="tt"><span class="cur">新品与热门商品</span><span>热销商品</span><span>热门即将推出</span><span>优惠</span></div>
        <!-- 新品与热门商品 -->
        <div class="tc show"><div id="box"><ul class="json_lst"></ul></div></div>
        <!-- 热销商品 -->
        <div class="tc"><a href="#"><img id="tc-img" src="../image/tc-img-1.png"></a></div>
        <!-- 热门即将推出 -->
        <div class="tc"><a href="#"><img id="tc-img" src="../image/tc-img-2.png"></a></div>
        <!-- 优惠 -->
        <div class="tc"><a href="#"><img id="tc-img" src="../image/tc-img-3.png"></a></div>
    </div>

    <!-- JavaScript -->
    <script src="../swiper/swiper-bundle.min.js"></script>
    <!-- 轮播图 -->
    <script>
        var swiper = new Swiper(".mySwiper", {
          slidesPerView: 3,
          spaceBetween: 20,
          scrollbar: {el: ".swiper-scrollbar",},
        });
    </script>
    <!-- 导航栏置顶 -->
    <script>  
        window.onscroll = function() {myFunction()};  
        function myFunction() {  
        var fixed = document.getElementsByClassName("fixed")[0];  
        fixed.style.top = "0px";
        }  
    </script>
    <!-- TAB选项卡 -->
    <script>
        var tab=document.getElementsByClassName("tab")[0];
        var tt=tab.querySelector(".tt");
        var span=tt.querySelectorAll("span");
        var tc=tab.querySelectorAll(".tc");
        //console.log(tab,tt,span,tc);
        for(var i=0;i<span.length;i++){
            span[i].index=i;
            span[i].onmouseover=function(){
                for(var j=0;j<tc.length;j++){
                    tc[j].style.display="none";
                    span[j].classList.remove("cur");
                }
                tc[this.index].style.display="block";
                this.classList.add("cur");
            }
        }
    </script> 
    <!-- JSON数据显示 -->
    <script>
        var json = [
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_1.jpg",
                name: "PUBG: BATTLEGROUNDS",
                des: "生存，射击，大逃杀，多人",
                price: "免费开玩"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_2.jpg",
                name: "Counter-Strike 2",
                des: "第一人称射击，射击，多人，竞技",
                price: "免费开玩"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_3.jpg",
                name: "使命召唤®",
                des: "第一人称射击，多人，射击，动作",
                price: " "
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_4.jpg",
                name: "THE FINALS",
                des: "多人，射击，破坏，第一人称射击",
                price: "免费开玩"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_5.jpg",
                name: "Dota 2",
                des: "免费开玩，多人在线战术竞技，多人，策略",
                price: "免费开玩"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_6.jpg",
                name: "房产达人 2",
                des: "模拟，设计与插画，建造，休闲",
                price: "HK$ 175.50"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_7.jpg",
                name: "Monster Hunter: World",
                des: "合作，多人，动作，开放世界",
                price: "HK$ 77.22"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_8.jpg",
                name: "Baldur's Gate 3",
                des: "角色扮演，选择取向，剧情丰富",
                price: "HK$ 399.00"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_9.jpg",
                name: "World of Warships",
                des: "海战，免费开玩，海军，二战",
                price: "免费开玩"
            },
            {
                link: "https://store.steampowered.com/",
                img: "../image/json_lst_10.jpg",
                name: "Granblue Fantasy Versus: Rising",
                des: "动作，2D格斗，动作角色扮演，单人",
                price: "HK$ 398.00"
            },
            
        ]
        var json_lst = document.querySelector(".json_lst");
        for (var v of json) {
            var nli = document.createElement("li");
            nli.innerHTML = `<div class="json-goods"><a href="${v.link}"><img src="${v.img}"></a></div><h3>${v.name}</h3><p class="json_des">${v.des}</p><p class="json_price">${v.price}</p>`;
            json_lst.appendChild(nli);
        }
        var box = document.getElementById('box');
        function hide() {box.style.display = "none";}
        function arise() {box.style.display = "block";}
    </script>
</body>
</html>
