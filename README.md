# LuckData-Douyin-API-Free
By using LuckData Douyin API, you can easily get hot video list, hot challenge list, total ranking list, user info, retweets, likes and comments, trending and so on.
# How to Use
Step 1: Click “Get Started”
Step 2: Purchase a plan and complete the payment
Step 3: Choose your preferred run mode
Step 4: Click "Test Endpoint"
# How to get a free Luckdata walmart API key?
Register for a Luckdata account and apply for the Douyin API. Luckdata will grant 100 free points for one month, which can be used with a limit of one request per second. If you need higher points and more request capacity, a paid version is required. Alternatively, you can wait for the next month to receive another 100 free points for use.
# GET Douyin rankings Code Snippets
## python
<pre>import requests

headers = {
    'X-Luckdata-Api-Key': 'your_luckdata_api_key'
}

json_data={}

response = requests.get(
    'https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223',
    headers=headers,
    
)
print(response.json())</pre>
## Java
<pre>import java.io.IOException;
import java.net.URI;
import java.net.http.HttpClient;
import java.net.http.HttpRequest;
import java.net.http.HttpResponse;

HttpClient client = HttpClient.newHttpClient();

HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223"))
    .GET()
    
    .setHeader("X-Luckdata-Api-Key", "your_luckdata_api_key")
    .build();

HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());</pre>
## go
<pre>package main

import (
  "fmt"
  "io"
  "log"
  "net/http"
  "strings"
)

func main() {
  client := &http.Client{}
  var data = nil
  req, err := http.NewRequest("GET", "https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223", data)
  if err != nil {
    log.Fatal(err)
  }
  
  req.Header.Set("X-Luckdata-Api-Key", "your_luckdata_api_key")
  resp, err := client.Do(req)
  if err != nil {
    log.Fatal(err)
  }
  defer resp.Body.Close()
  bodyText, err := io.ReadAll(resp.Body)
  if err != nil {
    log.Fatal(err)
  }
  fmt.Printf("%s\n", bodyText)
}</pre>
## shell
<pre>curl -X GET "https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223"  -H "X-Luckdata-Api-Key":"your_luckdata_api_key" </pre>

mroe
For more information about luckdata Douyin API, please click:<a href="https://luckdata.io/marketplace/detail/douyin-API">luckdata Douyin API</a>
