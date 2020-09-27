```python
<!DOCTYPE html>
<html>
    <title>first page</title>
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
            width: 29%;
            margin-left: 340px;
        }
        #right_q{
            width: 30%;
            float: right;
            margin-right: 200px;
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
            <h1>질문 1</h1>
            <h4>부모님한테 용돈을 받았습니다. 갖고 싶었던 옷이 세일 중이고, 오늘 저녁에 당장 먹고 싶은 음식이 있습니다.</h4>
        </div>
        <div id = "image">
            <img src = "http://img4.tmon.kr/cdn2/deals/2019/01/17/1768474370/front_13bd9_i2ph0.jpg" width = "300" height="300" id = "left">
            <img src = "https://img.khan.co.kr/news/2019/05/30/l_2019053101003584700279572.jpg" width = "300" height="300" id= "right">
        </div>
        <div  id = "left_q">
            <P><label><input type = "radio" name = "q1" value = "fashion">세일 중이면 당장 사야지~ 이런 기회를 놓칠 수 없어!</input></label></P>
        </div>
        <div id = "right_q">
            <P><label><input type = "radio" name = "q1" value = "food">저녁에 그거 먹을거야! 안 먹으면 큰일나...</input></label></P>
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
            gender = temp[1];
            var q1_data = document.getElementsByName("q1").length;
            if (document.getElementsByName("q1")[0].checked == false && document.getElementsByName("q1")[1].checked == false){
                    alert("항목을 선택해주세요");
            }else{
                for (var i=0; i < q1_data; i++) {
                    if (document.getElementsByName("q1")[i].checked == true) {
                        var ans_1 = document.getElementsByName("q1")[i].value;
                    }
                    location.href = "https://kang9366.github.io/bigcontest/second.html?" + ans_1;
                }
            }
        } 
    </script>
</html>
```
