```
<!DOCTYPE html>
<html>
    <title>fourth page</title>
    <meta charset="UTF-8">
    <style>
        #image{
            margin-top: 100px;
            margin: 0 auto;
        }
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
            width: 20%;
            margin-left: 420px;
        }
        #right_q{
            width: 30%;
            float: right;
            margin-right: 150px;
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
            <h1>질문 4</h1>
            <h4>당신은 드디어 취업에 성공했습니다. 자기의 보금자리를 꾸밀 차례입니다. 무엇부터 고려하겠습니까?</h4>
        </div>
        <div id = "image">
            <img src = "https://i.pinimg.com/originals/60/08/78/6008784c706a47c2f427b7e96f7403e6.jpg" width = "300" height="300" id = "left">
            <img src = "https://i.pinimg.com/originals/ee/a1/0c/eea10c2d70ae4c2c9795ccf129ba477d.jpg" width = "300" height="300" id= "right">
        </div>
        <div  id = "left_q">
            <P><label><input type = "radio" name = "q1" value = "house">자신의 집부터 꾸미기 시작한다. </input></label></P>
        </div>
        <div id = "right_q">
            <P><label><input type = "radio" name = "q1" value = "car">나만의 드림카를 찾는다.</input></label></P>
        </div>
        </br>
        <p><button type = "submit " id = "submitBtn" onclick = "value_check()">다음</button></p>
        <div id = "third">
        </br></br></br>
            <h3>-강원대학교 정미례 배정윤 박성흠 안정선, 한림대학교 강승구-</h3>
        </div>
    </body>
    <script>
        function value_check(){
            temp = location.href.split("?");
            data = temp[1].split(":");
            ans_1 = data[0];
            ans_2 = data[1];
            ans_3 = data[2];
            var q4_data = document.getElementsByName("q1").length;

            if (document.getElementsByName("q1")[0].checked == false && document.getElementsByName("q1")[1].checked == false){
                alert("항목을 선택해주세요");
            }else{
                for (var i=0; i < q4_data; i++) {
                    if (document.getElementsByName("q1")[i].checked == true) {
                        var ans_4 = document.getElementsByName("q1")[i].value;
                    }
                }
                location.href = "https://kang9366.github.io/bigcontest/fifth.html?" + ans_1 + ":" + ans_2 + ":" + ans_3 + ":" + ans_4;
            }
        } 
    </script>
</html>
```
