### Hi there 👋

꾸준하게 노력하는,<br>
배움을 나누며 소통하는,<br>
목표를 이루기 위해 성장하는,<br>
개발자 되기!<br>
### aws 인스턴스 성능테스트 (micro, nano, small, medium 순)
* 성능 테스트 크롤링 코드
```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    import requests
    from bs4 import BeautifulSoup

    # 여러 웹사이트의 URL 리스트
    urls = ['https://github.com/yeahh315',
            'https://github.com/Chaeniiiii',
            'https://github.com/Johyerin',
            'https://github.com/Woo-Shinyoung',
            'https://github.com/dbqudals',
            'https://github.com/kihyun1221',
            'https://github.com/seungtoctoc'
             ]
    
    result = ""

    for url in urls:
        # 각 웹사이트의 내용을 가져오기
        response = requests.get(url)

        # 가져온 내용을 BeautifulSoup을 사용하여 파싱
        soup = BeautifulSoup(response.text, 'html.parser')

        # <article> 태그 찾기
        article_tag = soup.find('article')
        name = soup.find('div', class_="vcard-names-container float-left js-profile-editable-names col-12 py-3 js-sticky js-user-profile-sticky-fields")
        
        result += url + "<br>"

        if name.text:
            result += name.text + "<br>"
        
        if article_tag:
            result += article_tag.text
        result += "<br>--------------------------------------------------<br><br>"

    if result:
        return result
    
    return ''



if __name__ == '__main__':
    app.run(host='0.0.0.0')

```
<br>

* Tg4 인스턴스 <br><br>
이러한 인스턴스는 기본 수준의 CPU 성능 외에 버스트 기능이 있어 워크로드에 필요한 만큼 성능을 높일 수 있습니다. 무제한 인스턴스는 필요할 때마다 원하는 기간 동안 높은 CPU 성능을 유지할 수 있습니다. 자세한 내용은 성능 순간 확장 가능 인스턴스 섹션을 참조하세요. 이러한 인스턴스는 다음의 경우에 적합합니다.<br><br>

    웹 사이트 및 웹 애플리케이션: <br>
    코드 리포지토리 <br>
    개발, 빌드, 테스트 및 스테이징 환경<br>
    마이크로서비스 <br><br>
    

* 인스턴스 별 성능 결과 <br><br>
<img width="444" alt="스크린샷 2024-01-04 오후 4 43 00" src="https://github.com/godltjsdud/godltjsdud/assets/71091090/a608481d-b5b9-45b2-be9c-61ce13ebd703"><br>
<img width="442" alt="스크린샷 2024-01-04 오후 4 35 46" src="https://github.com/godltjsdud/godltjsdud/assets/71091090/0875c67a-95e9-406a-99f3-ee7447939c8c"><br>
<img width="448" alt="스크린샷 2024-01-04 오후 4 29 42" src="https://github.com/godltjsdud/godltjsdud/assets/71091090/622e8732-2791-4a40-81ee-ba37289ec929"><br>
<img width="441" alt="스크린샷 2024-01-04 오후 4 51 42" src="https://github.com/godltjsdud/godltjsdud/assets/71091090/3a43c96a-01a1-4688-a4f9-13f45a2422b6"><br>
```
  t4g.micro : 5789ms 
  t4g.nano : 5989ms 
  t4g.small : 5810ms 
  t4g.medium :  6149ms

  micro < small < nano < medium
```
<br>

* 하드웨어 사양<br>
    | 인스턴스 유형 | 기본 vCPU | 메모리(GIB) |
    | ------- | ------- | ------- |
    | t4g.nano | 2 | 0.50 |
    | t4g.micro | 2 | 1.00 |
    | t4g.small | 2 | 2.00 |
    | t4g.medium | 2 | 4.00 |
<br><br>

<!--
**godltjsdud/godltjsdud** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:
- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

<!-- 조회수 -->
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fgodltjsdud&count_bg=%23000000&title_bg=%23FFC0C0&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://github.com/godltjsdud)

<!-- 깃헙리드미스탯, 백준 -->
<img src="https://github-readme-stats.vercel.app/api?username=godltjsdud&show_icons=true&theme=ambient_gradient" width="400px">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src= "http://mazassumnida.wtf/api/v2/generate_badge?boj=godltjsdud">

<br>

## ⚒️ Skills
<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"> <!-- java -->
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> <!-- python -->
<img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> <!-- html5 -->
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> <!-- css -->
<img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> <!-- css -->
<img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white"> <!-- jquery -->
<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <!-- mysql -->
<img src="https://img.shields.io/badge/firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white"> <!-- firebase -->
<img src="https://img.shields.io/badge/node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"> <!-- node.js -->
<img src="https://img.shields.io/badge/django-092E20?style=for-the-badge&logo=django&logoColor=white"> <!-- django -->
<img src="https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white"> <!-- flask -->
<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=white"> <!-- react -->
<img src="https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <!-- spring -->
<img src="https://img.shields.io/badge/linux-FCC624?style=for-the-badge&logo=linux&logoColor=black">
<img src="https://img.shields.io/badge/apache tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=white">
<img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">

<br>

##  🏆 Awards

| PERIOD | COMPETITON | AWARDS |
| ------- | ------- | ------- |
| 2023.11.16 | **제21차 동북아 공개SW활성화포럼** | **Outstanding Technologies Project Award 🏆** |
| 2022.12.06 | **제 16회 공개SW 개발자대회** | **학생부문 대상 🥇 (과학기술정보통신부 장관상)** |
| 2022.09.23 | 제 18회 한성 공학경진대회 | 작품부문 대상 🥇, 특허부문 금상 🥇 |
| 2022.06.03 | 컴퓨터공학부 캡스톤디자인 작품 발표회 | 모바일분야 최우수상 🥇 |
| 2022.10.07 | 22-1 한성대학교 창의융합성과 경진대회 (C&C Festival) | 금상🥈 |
| 2021.09.24 | 제 17회 한성공학경진대회 | 작품부문 금상 🥈, 특허부문 동상 🥉 |


