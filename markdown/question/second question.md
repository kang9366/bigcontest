```
<!DOCTYPE html>
<html>
    <title>second page</title>
    <meta charset="UTF-8">
    <style>
        #left{
            float: left;
            margin-left: 400px;
        }
        #right{
            float: right;
            margin-right: 400px;
        }
        #left_q{
            float: left;
            width: 30%;
            margin-left: 330px;
        }
        #right_q{
            width: 30%;
            float: right;
            margin-right: 170px;
        }
        #submitBtn {
            border-top-left-radius: 8px;
            border-bottom-left-radius: 8px;
            border-top-right-radius: 8px;
            border-bottom-right-radius: 8px;
            width: 150px;
            height: 40px;
            font-size: 20px;
            margin-top: 100px;
            margin-left: 45%;
            margin-right: 30%;
        }
        #btn button:hover{
            color : white;
            background-color: black;
        }
        #question{
            width: 100%;
            height: 100px;
            background-color: #E3F6CE;
            margin-bottom: 80px;
            text-align: center;
        }
        #third{
        text-align: center;
        }
    </style>

    <body>
        <div id = "question">
            <h1>질문 2</h1>
            <h4>친구들이랑 오랜만에 만나는데 어디를 예약할까?<h4>
        </div>
        <div id = "image">
            <img src = "https://pbs.twimg.com/profile_images/2724959951/4d210c67ac5bb270227129cff31655b1_400x400.jpeg" width = "300" height="300" id = "left">
            <img src = "https://img7.yna.co.kr/etc/inner/KR/2020/04/17/AKR20200417158000004_02_i_P2.jpg" width = "300" height="300" id= "right">
        </div>
        <div id = "left_q">
            <p><label><input type = "radio" name = "q1" value = "picnic">다같이 당일치기(콘서트/전시회/야구장)로 알차게 놀자!</input></label></p>
        </div>
        <div id = "right_q">
            <p><label><input type = "radio" name = "q1" value = "camping">1박2일로 (캠핑, 스키장) 밤새자!</input></label></p>
        </div>
        </br>
        <p><button type = "submit " id = "submitBtn" onclick = "value_check();",  herf>다음</button></p>
        <div id = "third">
        </br></br></br>
            <h3>-강원대학교 정미례 배정윤 박성흠 안정선, 한림대학교 강승구-</h3>
        </div>
    </body>
    <script>
        function value_check(){
            temp = location.href.split("?");
            ans_1 = temp[1];
            var q2_data = document.getElementsByName("q1").length;

            if (document.getElementsByName("q1")[0].checked == false && document.getElementsByName("q1")[1].checked == false){
                    alert("항목을 선택해주세요");
            }else{
                for (var i=0; i < q2_data; i++) {
                    if (document.getElementsByName("q1")[i].checked == true) {
                        var ans_2 = document.getElementsByName("q1")[i].value;
                    }
                    location.href = "https://kang9366.github.io/bigcontest/third.html?" + ans_1 + ":" + ans_2;
                }
            }
        } 
    </script>
</html>
```
