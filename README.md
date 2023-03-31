## 넷플릭스 소개 html

넷플릭스에 대해 소개하는 간단한 html 입니다. 
android studio 와 cordova 를 이용하여 에뮬레이터에 hybrid html 페이지를 표시하기 위해 만들었습니다.

  ![start](https://user-images.githubusercontent.com/88778903/229040567-7309e881-7c61-4653-9c49-ff14f558e1d7.PNG)

페이지의 첫 화면은 위와 같이 이루어져 있습니다

  ![chart](https://user-images.githubusercontent.com/88778903/229040572-16ca9f9f-214a-4d0d-80ca-8bc95ed9a6a7.PNG)

* 넷플릭스 소개
  * 소개
  * 역사
  * 요금제
  * 차트

  ![movie](https://user-images.githubusercontent.com/88778903/229040571-9cc554d0-3893-4aac-9ef7-05dad196c8b2.PNG)

* 넷플릭스 관련 영상
  * 넷플릭스 소개 영상
  * 넷플릭스 인트로 영상

  ![location](https://user-images.githubusercontent.com/88778903/229040576-04baf8d7-97cf-4d5a-b8b7-20c128a0d544.PNG)

* 넷플릭스 소재지
  * 넷플릭스 본사 소재지 구글 맵 
  * 넷플릭스 한국 소재지 구글 맵

  ![poster](https://user-images.githubusercontent.com/88778903/229040579-bef28681-3a5b-45dd-89ac-4e04efc93351.PNG)


* 넷플릭스 포스터 갤러리
  * 넷플릭스 포스터 이미지들

로 이루어져 있습니다.

---

bootstrap framework 와

```html
          <div style="text-align: center">
            <img src="./img/unnamed.png" width="10%" class="rounded-circle"> 
            <!-- 부트스트랩 -->
          </div>
```

chart.js 를 사용하였 습니다.

---


```html
          <div data-role="collapsible">
              <h3>넷플릭스 글로벌 가입자 인원 차트</h3>
              <p>
                <canvas id="myChart" width="100%"></canvas>
                <script type="text/javascript">
                  var context = document
                      .getElementById('myChart')
                      .getContext('2d');
                  var myChart = new Chart(context, {
                      type: 'bar', // 차트의 형태
                      data: { // 차트에 들어갈 데이터
                          labels: [
                              //x 축
                              '2010','2012','2017','2018','2019','2020','2021', '2022'
                          ],
                          datasets: [
                              { //데이터
                                  label: '넷플릭스 글로벌 가입자 인원 ( 1/10000 명 단위)', //차트 제목
                                  fill: false, // line 형태일 때, 선 안쪽을 채우는지 안채우는지
                                  data: [
                                      2000,3300,10900,13900,16700,20400,22180,22160 //x축 label에 대응되는 데이터 값
                                  ],
                                  backgroundColor: [
                                      //색상
                                        '#E50914',
                                        '#E50914',
                                        '#E50914',
                                        '#E50914',
                                        '#E50914',
                                        '#E50914',
                                        '#E50914',
                                        '#E50914',
                                  ],
                                  borderWidth: 2 //경계선 굵기
                              }/* ,
                              {
                                  label: 'test2',
                                  fill: false,
                                  data: [
                                      8, 34, 12, 24
                                  ],
                                  backgroundColor: 'rgb(157, 109, 12)',
                                  borderColor: 'rgb(157, 109, 12)'
                              } */
                          ]
                      },
                      options: {
                          scales: {
                              yAxes: [
                                  {
                                      ticks: {
                                          beginAtZero: true
                                      }
                                  }
                              ]
                          }
                      }
                  });
              </script>
              </p>
            </div>
```

