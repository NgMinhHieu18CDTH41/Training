<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
   <link href="/dist/css/btr-menu.css" rel="stylesheet" />
   <link rel="stylesheet" href="css/style.css">
   <link rel="stylesheet" type="text/css" href="css/bootstrap.min.css">
   <script type="text/javascript" src="js/bootstrap.min.js"></script>
   <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.1/css/all.css">
   <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
   <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
   <script src="js/js.js"></script>
     <title>Marketing facebook ?</title>
    
 <script>
        document.addEventListener("DOMContentLoaded",function(){
             var nut = document.querySelector('div.icon i');    
             var mobile = document.querySelector('ul');
             nut.addEventListener('click',function(){
                 mobile.classList.toggle('active');
             })
         })
 </script>
 </head>
 <body>
 <div id="header">
         
         <nav id="site-navigation" class="main-navigation"> 
         <li><a  style="text-decoration: none;" href="http://localhost:88/minhhieu1/webtintuc1/Admin/login.php" target="t_bank">Admin</a></li>
           <ul>
           <li><a style="text-decoration: none;" href="http://localhost:88/minhhieu1/webtintuc1/Admin/public.php">Home</a></li>
           <li><a style="text-decoration: none;" href="gioithieu.php">Intro</a></li>
           <li><a  style="text-decoration: none;" href="ads.php">Advertisement</a></li>
             <?php  
             include 'config.php'; 
                   $str = "SELECT * FROM `loaitin` WHERE idLT = 17";
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       ?>
                           
                           <li><a  style="text-decoration: none;"href="unlock.php?id=<?php  echo $row['idLT'];?>"><?php echo $row ['TenDV'];   ?> </a></li>
                   <?php } ?>
                   <?php  
             include 'config.php'; 
                   $str = "SELECT * FROM `loaitin` WHERE idLT = 18";
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       ?>
                           
                           <li><a  style="text-decoration: none;"href="like.php?id=<?php  echo $row['idLT'];?>"><?php echo $row ['TenDV'];   ?> </a></li>
                   <?php } ?>
                   <?php  
             include 'config.php'; 
                   $str = "SELECT * FROM `loaitin` WHERE idLT = 19";
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       ?>
                           
                           <li><a  style="text-decoration: none;"href="follow.php?id=<?php  echo $row['idLT'];?>"><?php echo $row ['TenDV'];   ?> </a></li>
                   <?php } ?>
           <li>
           <a style="text-decoration: none;" href="fl.php">Type of service</a>
           <ul class="cap_2">
           <?php    
          
                   $str = "SELECT * FROM `tin` WHERE idTL = 1";
                
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                    if($row['idTin'] == 1){
                       ?>
                     <li><a  style="text-decoration: none;" href="#project" ><?php echo $row ['tentin'];  ?> </a></li>

                     <?php
                     }else{ ?> <li><a  style="text-decoration: none;" href="ads.php?id=<?php  echo $row['idTin'];?>" ><?php echo $row ['tentin'];  ?> </a></li>
                    
                      
                   <?php }} ?>
                   <?php    
          
                   $str = "SELECT * FROM `tin` WHERE idTL = 2";
                
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       if($row['idTin'] == 3){
                        ?>
                      <li><a  style="text-decoration: none;" href="#unlock" ><?php echo $row ['tentin'];  ?> </a></li>
 
                      <?php
                      }else{ ?> <li><a  style="text-decoration: none;" href="unlock.php?id=<?php  echo $row['idTin'];?>" ><?php echo $row ['tentin'];  ?> </a></li>
                     
                       
                    <?php }} ?>
                   <?php    
          
                   $str = "SELECT * FROM `tin` WHERE idTL = 3";
                
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       if($row['idTin'] == 10){
                        ?>
                      <li><a  style="text-decoration: none;" href="#liked" ><?php echo $row ['tentin'];  ?> </a></li>
 
                      <?php
                      }else{ ?> <li><a  style="text-decoration: none;" href="like .php?id=<?php  echo $row['idTin'];?>" ><?php echo $row ['tentin'];  ?> </a></li>
                     
                       
                    <?php }} ?>

          </li>   
        </ul>
       
        <!-- <li><a  style="text-decoration: none;" href="ads.html">CHẠY QUẢNG CÁO</a></li> -->
       
     </ul>
           <div class="icon">
               <i class="fas fa-bars"></i>
           </div>
       </nav>
   </div><!--header-->
   <div id="slider">
         <div class="container-fluid">
            <div class="row">
              <div class="w3-content w3-section" style="max-width:100%">
          
                <img class="mySlides" src="img/sl3.jpg" >
                <img class="mySlides" src="img/fb111.png ">
              
        
          
        </div>
        </div> 
        </div>
           <script>
        var myIndex = 0;
        carousel();
        
        function carousel() {
          var i;
          var x = document.getElementsByClassName("mySlides");
          for (i = 0; i < x.length; i++) {
            x[i].style.display = "none";  
          }
          myIndex++;
          if (myIndex > x.length) {myIndex = 1}    
          x[myIndex-1].style.display = "block";  
          setTimeout(carousel, 3000); // Change image every 3 seconds
        }
        </script>
 </div>   <!-- slider -->
 <div id="topnews">
    <div class="">
       <div class="row">
          
              <div class="col-md-4 col-xs-12">
                 <p class="p1">
                     <img src="img/ADSSS.jpg" width="400" height="300">
                   </p>
                   <h3 class="tieude"><i class="fas fa-ad"></i>  Advertisement </h3>
                   <p class="p1">Chạy quảng cáo Facebook là hình thức quảng cáo trả phí để hiển thị hình ảnh quảng cáo trên Facebook.<br>
                   </p>
                   <a href="ads.php"><div class="css-bor"><button class="btn" type="button">Xem thêm</button></div></a>
              </div>
              <div class="col-md-4 col-xs-12">
                 <p class="p1">
                     <img src="img/uns.jpg" width="400" height="300">
                   </p>
                   <h3 class="tieude"><i class="fas fa-unlock"></i> UNLOCK ACCOUNT</h3>
                   <p class="p1">Mở khóa tất cả các loại. Mất thông tin, quên mật khẩu .Các loại dính Checpoin,FAQ , FAQ Apps ,bắt xác minh danh tính<br>
                   </p>
                   <a href="unlock.php"><div class="css-bor"><button class="btn" type="button">Xem thêm</button></div></a>
               </div>
               <div class="col-md-4 col-xs-12">
                   <p class="p1">
                       <img src="img/LIKEĂ.jpg" width="400" height="300">
                     </p>
                     <h3 class="tieude"><i class="far fa-thumbs-up"></i> TĂNG LIKE ,SUB</h3>
                     <p class="p1">Tăng like, comment, follow là một hình thức cũng khá phổ biến hiện nay trên mạng xã hội..........
                         <br>
                     </p>
                     <a href="like.php"><div class="css-bor"><button class="btn" type="button">Xem thêm</button></div></a>
                 </div>
          
       </div>
           </div>
    </div><!-- topnews -->  
    <div id="project">
    <div class="txt-align-c ">
    <a style="text-decoration: none;" href="ads.php" class="color-black">
        
    <h2 style="text-align: center;">
    <?php  
                   $str = " SELECT * FROM `tin` WHERE idTL = 1 ";
                 
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       ?>
                     <li><a  style="text-decoration: none;" href="ads.php?id=<?php  echo $row['idTin'];?>" ><?php echo $row ['tentin'];    ?> </a></li>
                      
                   <?php } ?>
    </h2>
    
    </a>
    </div>
    <div class="content-item row">
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
             <a href="ads.php"><img src="img/ads11.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>   
            </div>
            
            
        </div>
    </div>
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
            <a href="ads.php"><img src="img/ads11.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>   
            </div>
           
        </div>
    </div>
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
            <a href="ads.php"><img src="img/ads11.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>   
            </div>
           
        </div>
    </div>
    </div>
    </div><!--project-->
    <div id="unlock">
    
    <div class="txt-align-c ">
    <a style="text-decoration: none;" href="unlock.php" class="color-black">
        <h1>
        <?php  
                   $str = " SELECT * FROM `tin` WHERE idTL = 2 ";
                 
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       ?>
                     <li><a  style="text-decoration: none;" href="unlock.php?id=<?php  echo $row['idTin'];?>" ><?php echo $row ['tentin'];    ?> </a></li>
                      
                   <?php } ?>
        </h1>
    </a>
    </div>
    <div class="content-item row">
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
             <a href="unlock.php"><img src="img/unlockfb.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>   
            </div>
            

        </div>
    </div>
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
            <a href="unlock.php"><img src="img/unlockfb.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a> 
            </div>
           
        </div>
    </div>
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
            <a href="unlock.php"><img src="img/unlockfb.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a> 
            </div>
            
        </div>
    </div>
    </div>
    </div>
    <div id="liked">
    
    <div class="txt-align-c ">
    <a style="text-decoration: none;" href="like.php" class="color-black" title=" Like , tương tác">
        <h1>
        <?php  
                   $str = " SELECT * FROM `tin` WHERE idTL = 3 ";
                 
                   $result = mysqli_query($conn, $str);
                   $i = 0;
                   while ( $row = mysqli_fetch_assoc($result) ){  
                       $i ++;
                       ?>
                     <li><a  style="text-decoration: none;" href="like.php?id=<?php  echo $row['idTin'];?>" ><?php echo $row  ['tentin'];    ?> </a></li>
                      
                   <?php } ?>
        </h1>
    </a>
    </div>
    <div class="content-item row">
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
             <a href="like.php"> <img src="img/likethui.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>  
            </div>
            
           
        </div>
    </div>
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
            <a href="like.php"> <img src="img/likethui.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>  
            </div>
         
        </div>
    </div>
    <div class="col-sm-4 c-i-sub">
        <div class="c-i-sub-sub">
            <div class="txt-align-c mar-bottom-10">
            <a href="like.php"> <img src="img/likethui.jpg" class="wid-8" title="tài khoản Facebook khi bị khóa"></a>  
            </div>
           
        </div>
    </div>
    </div>
    </div><!-- liked -->
    <div class="footer" >
       
            <div class="footer-info"> 
        
                <strong>MinhHieu69 Entertainment&nbsp;</strong></span></p><p><span >
                    <strong>Điện thoại:</strong> 
                    (0965) 1.988 97 &nbsp;<strong>Fax:
                    </strong>  (0965) 1.988 97
                </span></p><p><span ><strong>Địa chỉ:&nbsp;
                </strong> Bình An I - Xã Lộc Vĩnh - Huyện Phú Lộc - Tỉnh Thừa Thiên Huế
            </span></p><p><span ><strong>Email:
            </strong>&nbsp;<span >
                  <a data-mce-href="mailto:minhhieu336a@gmail.com" href="mailto:minhhieu336a@gmail.com">
                <span >mailinh13a@gmail.com</span></a>
            </span>
                    </span></p
                        ><p><span><strong>Website:</strong>&nbsp;
                  <a  class= "wed"href=""  data-mce-href="">http://doanxem.com.vn</a>
                    </span>
                    </p>
                <div class="bottom">
                    <table >
                          <a href="https://www.facebook.com/0609NMH"><img src="http://bangwater.vn/files/assets/icon3.png" alt="icon1"> </a>
                        <img src="http://bangwater.vn/files/assets/icon4.png" alt="icon2">
                        <img src="http://bangwater.vn/files/assets/icon2.png" alt="icon3">
                        <img src="http://bangwater.vn/files/assets/icon1.png" alt="icon4">
                
                
                    </tr>
                    </table>
                </div>
            </div>
        </div><!-- footer -->
</body>
</html>
