# Multi-Functional_LINE_Notify_BOT
This is a multi-functional messaging program that connects to the LINE Notify API on Colab. As long as you provide LINE Notify tokens, it can send messages, LINE stickers and images out as "LINE Notify". What's more, you can even send messages at specific times.

<a href="https://colab.research.google.com/drive/1MV0YjvmYPfyehyKZiATdEZkiw0fBmXWv?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="google colab logo"></a>
 ㅤ
### :star: If this project is helpful to you, please help star this repo. Thanks! :hugs:
 ㅤ
## Preparison
To use this project, please copy your LINE Notify token first (obtain from [here](https://notify-bot.line.me/my/)). Otherwise, you need a Google account for accessing to your Google Drive, along with one (or more) "name+ (TAB)+LINE Notify token" stored row by row in a txt named `LineNotifyTokens.txt` in `/content/drive/MyDrive` of your Google Drive.

 ㅤ
<p align="center">
  <img src="pic/txt.jpg" width=500>
  <br>
  <em>▲ Example of LineNotifyTokens.txt ▲</em>
  <br>
</p>

 ㅤ
 
:bell: The left side of each row in `LineNotifyTokens.txt` is the name of token named by your own and the right one is token, which are separated by TAB(\t).

 ㅤ
## Installation

There is **NO** installation required for this project. (Precisely, installations will be processed in Colab notebook).

**Just open the Colab notebook** and run the code from top to bottom by clicking play buttons on the left side one by one! 

 ㅤ
<p align="center">
  <img src="pic/play button.jpg" width=500>
  <br>
  <em>▲ Play buttons on the left side. ▲</em>
  <br>
</p>
 ㅤ
 
## How to Use After Running the Code?
##### :warning: Parameters IN a cell must be set before running the cell, whereas those BELOW a cell don't. :warning:

 ㅤ
 
1. Choose the token number you want to send messages with in cell `Tokens`, where all token numbers will be listed below.

 ㅤ
 
2. Set message to send in cell `Set Message to Send`. Besides, you can set sticker to send by ticking `add_sticker` and fill in `sticker_package_id` & `sticker_id` if you wanna send a sticker with your message.

 ㅤ ㅤ:bell: You can find sticker package id & sticker id in [this website](https://developers.line.biz/en/docs/messaging-api/sticker-list/#sticker-definitions). 

 ㅤ
 
3. Choose the way ("Upload"/"URL"/"Google Drive Path") to provide image in cell `Set Image to Send`:
   - If you choose **URL**, please provide image URL in `image_url`
   - If you choose **Google Drive Path**, please provide image Google Drive Path in `Google_Drive_Path`
   - If you choose **Upload**, please upload image(s) below the cell by clicking upload button. (This is the only way to send multiple images.)

 ㅤ ㅤ:bell: You can skip this step if you're not going to send any image.

 ㅤ
 
4. Set when to send after ticking `send_at_the_appointed_time` in cell `Set When to Send` if you don't wanna send the message immediately.

 ㅤ ㅤ:bell: You can skip this step if you're not going to send the message immediately.
 
 ㅤ

5. Click button `Send!` below cell `Send Message!` to send message & image(s)!
 
 ㅤ
## FAQ
:question: Cannot find `LineNotifyTokens.txt` in connected Google Drive since it doesn't exsist.

:bulb: Actually, tokens can be read from Google Sheet as well if there's a Google Sheet API file named GSheet.json in `/content/drive/MyDrive` of your Google Drive and your LINE Notify tokens and their names are stored in a Google Sheet row by row which already connects to Google Sheet API, which is convenient to edit on the smartphone. Provide the Google sheet id by opening the group in Colab named `Preprocessing` and fill it in `sheet_id` to do so. However, I suggest you to create a txt file with your own LINE Notify tokens and their names and upload it to your Google Drive, which may be a faster way to solve this problem. Or you can just key in an usable LINE Notify token and fill it in `LINE_Notify_API_token` if you don't wanna provide LINE Notify API tokens from Google Drive, which may be the fastest way to solve this problem while it's a little inconvenient for those having many tokens to choose.

 ㅤ
<p align="center">
  <img src="pic/gs.jpg" width=500>
  <br>
  <em>▲ The format of Google Sheet, where LINE Notify API tokens and their name are stored. ▲</em>
  <br>
  <br>
  <img src="pic/sheet_id.jpg" width=500>
  <br>
  <em>▲ You can fill in the Google sheet id here or change the path of LineNotifyTokens.txt and the one of API key (.json file) of Google Sheet. ▲</em>
  <br>
</p>
 ㅤ
 
:question: Something different from the above.

:bulb: Send mail to pikasxyz@gmail.com and explain in detail.

 ㅤ 
## Reference

1. [List of available stickers | LINE Developers](https://developers.line.biz/en/docs/messaging-api/sticker-list/#sticker-definitions)
2. [LINE Notify](https://notify-bot.line.me/my/)
