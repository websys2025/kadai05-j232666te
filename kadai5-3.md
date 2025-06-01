## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能：
　郵便番号を入力すると、該当する地域の「都道府県」「市区町村」などの情報を返す機能
* リクエストとレスポンスのフォーマット：
　・リクエスト：fetch(`${endpoint}?zipcode=${zipcode}`)
　・レスポンス：const resultText = `住所: ${address.address1} ${address.address2} ${address.address3}`;
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL：
Open-Meteo API
* エンドポイントと機能
　指定した緯度・経度の現在の天気を返す機能
* リクエストとレスポンスのフォーマット
　・リクエスト：const url = `https://api.open-meteo.com/v1/forecast?latitude=${latitude}&longitude=${longitude}&current_weather=true`;
　・レスポンス：const resultText = `
                            <b>現在の天気（千葉）：</b><br>
                            天気：${getWeatherDescription(weather.weathercode)}<br>
                            気温：${weather.temperature}℃<br>
                            風速：${weather.windspeed} km/h<br>
                            観測時刻：${weather.time}<br><br>
                        `;
### Q3-3. 感想
* 今回の課題で苦労したこと
　初めてAPIを使ったため、エンドポイントの指定方法や、非同期通信（fetch）の使い方に戸惑った。
* 演習を通して理解できたこと
　Web APIの基本的な使い方、JSON形式で返ってきたデータの解析方法、APIから取得したデータをHTMLに表示する方法など、実際に　動かしながら学ぶことができた。
* Web APIの利便性や課題など
　APIを使えば、外部のデータを簡単に活用でき、Webアプリの幅が広がると実感した。一方で、認証やセキュリティ面の理解も必要だ　と感じた。

