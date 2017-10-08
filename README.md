# iUESC
An online education paid website 

1.项目描述：

   《iUESC》— Ultimate Education of south china是一个在线教学网站，以计算机科学与技术为主，包括：原创作品的发布、报酬比例的增长、直播教学、科技资讯及前辈在线指导。

2.开发环境：

    Windows 8.1 x64/Sublime Text3/FireBug/Multibrowser/MyEclipse 10/Tomcat 7/JDK 7。(建议)

3.核心技术：

    Html5/Css3/JavaScript/JQuery/Bootstrap/JSP/Mysql。（建议）

4.项目说明：

>>iuesc's Readme.text {
1.Question's outlines : 
@author : jettle 2017-08-29
@title : javascript如何获取EL表达式中的值？
@description : 当用户登录系统时，如果，系统验证用户信息成功，则将用户信息存储于Session中（request.getSession().setAttribute("login_user",u);），再通过jsp中的${sessionScope.login_user.name}来获取用户信息，EL表达式中的值来判断用户是否登录系统，若：if（EL表达式）==true，则做出相应的网页改变，如：文字颜色，内容的改变等等。
[keywords : jsp/session/EL表达式/javascript]

2.JSP's codes :
       <li>
               <a href="login.jsp" id="LoginText"><span class="glyphicon glyphicon-user"></span><strong id="LoginStrong">注册/登录</strong>${sessionScope.login_user.name}</a>
               <script type="text/javascript">
               window.onload = function(){
                 var num = "${sessionScope.login_user.name}";
                 if(num){
                      document.getElementById("LoginStrong").innerHTML = "欢迎：";
                      document.getElementById("LoginText").style.color = "red";
                   }
                   
               }
               </script>
            </li>
3.Methods : 在javascript中使用变量存储EL表达式的值，即：var num = "EL表达式";。

4.Conclutions : 建议探究javascript/jsp/servlet之间的执行原理。
}


>>iuesc's Readme.text {
    
1.Question's outline : 
@author : jettle 2017-08-29
@title : javascript如何改变jsp中a标签的herf属性？
@description ：在通过EL表达式的值确定为：用户已登录，来改变对应的a标签的herf属性，目的：当用户未登录时，点击a标签跳转至login.jsp（登录页面）；当用户已登录时，点击a标签跳转至person.jsp（个人主页）。
[keywords : javascript/jsp-a-herf/EL表达式/]

2.JSP's codes : 
<li>
               <a href="login.jsp" id="LoginText"><span class="glyphicon glyphicon-user"></span><strong id="LoginStrong">注册/登录</strong>${sessionScope.login_user.name}</a>
               <script type="text/javascript">
               window.onload = function(){
                 var num = "${sessionScope.login_user.name}";
                 if(num){
                      document.getElementById("LoginStrong").innerHTML = "欢迎：";
                      document.getElementById("LoginText").style.color = "red";
                      document.getElementById("LoginText").href = "person.jsp";
                   }
                   
               }
               </script>
            </li>

3.Methods : javascript中通过document.getElementById("LoginText").href = "person.jsp";（LoginText为a标签的id值）实现js改变a标签href属性。

4.Conclusions ：应熟悉html的Dom树，及其结点的获取，javascript在一定程度上，都是对Dom树结点的改变，来实现html的动态性。

}
}
