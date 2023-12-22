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
