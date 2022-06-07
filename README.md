#HTML
    <div class="side-bar">
        <div class="close-menu"><span class="close">X</span></div>
        <div class="wrapper-side-bar">
            <div class="nav-side-bar">
                <ul>
                    <li><a href="#">QUẢN LÝ CRUSH</a></li>
                    <li><a href="#">HƯỚNG DẪN</a></li>
                    <li><a href="#">LỊCH SỬ</a></li>
                    <li><a href="#">QUÀ NHẬN ĐƯỢC</a></li>
                </ul>
            </div>
            
        </div>
    </div>
 
 
 
 #CSS
 .wrapper-side-bar ul {
    list-style: none;
}

.wrapper-side-bar ul li {
    background: #33383e;
    padding: 20px;
    display: block;
}

.wrapper-side-bar ul li:hover {
    background: #202222;
}

.wrapper-side-bar ul li a {
    color: white;
    text-decoration: none;
    font-family: Arial, Helvetica, sans-serif;
}

.side-bar {
    position: absolute;
    opacity: 0;
    width: 100%;
    height: 100%;
    top: 0;
    left: -400px;
    overflow: hidden;
    position: fixed;
    background: #33383e;
    z-index: 999;
    transition: 0.5s;
}

.enter {
    opacity: 1;
    left: 0;
}

.close-menu {
    color: white;
    margin: 3%;
    text-align: right;
}
.close{
    cursor: pointer;
}


#JAVASCRIPT
<script>
        $("#side-bar-button").click(function () {
            $("#side-bar-button").css("opacity", "0");
            $(".side-bar").addClass("enter");
        })

        $(".close").click(function () {
            $(".side-bar").removeClass("enter");
            $("#side-bar-button").css("opacity", "1");
        }) 
    </script>
