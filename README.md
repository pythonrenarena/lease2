# lease2
<html>
  <html lang="ja">
  <head>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="https://pyscript.net/latest/pyscript.css" />
    <script defer src="https://pyscript.net/latest/pyscript.js"></script>
  </head>
  <body>
    <py-script>
      from datetime import datetime
      now = datetime.now()
      print(f"今は{now:%Y年%m月%d日 %H:%M:%S}です。")
      price=input("リース債務残高")
      rate=input("割引率")
      period=input("リース期間")
      fee=input("年間リース料")
    </py-script>
  </body>
</html>
