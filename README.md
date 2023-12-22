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
      print("リース債務残高:"+price+"円、割引率:"+rate+"%、年数:"+period+"年、年間リース料:"+fee+"円")

year=1
      
balance=price
deptotal=0

print(str(year)+"年目期首")
print("　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　")
print("リース資産"+str(price)+"/リース債務"+str(balance))
print("（BS　リース債務合計額:"+str(balance)+"）")
while int(year)<int(period):

 print("---------------------------------------")


 interest=round(int(balance)*int(rate)/100)
 repayment=int(fee)-int(interest)
 balance=int(balance)-int(repayment)
 dep=round(int(price)/int(period))
 deptotal=dep+deptotal

 print(str(year)+"年目期末")
 print("　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　")
 print("支払利息"+str(interest)+"/現金預金"+str(fee))
 print("リース債務"+str(repayment))

 print("（BS　リース債務合計額:"+str(balance)+"）")
 print("　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　")
 print("減価償却費"+str(dep)+"/減価償却累計額"+str(dep))

 print("（BS　減価償却累計額:"+str(deptotal)+"）")

 year=year+1


print("---------------------------------------")

repayment=int(balance)
interest=int(fee)-int(repayment)
balance=0
dep=round(int(price)/int(period))
deptotal=dep+deptotal

print(str(year)+"年目期末")
print("　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　")
print("支払利息"+str(interest)+"/現金預金"+str(fee))
print("リース債務"+str(repayment))

print("（BS　リース債務合計額:"+str(balance)+"）")

print("　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　")

print("減価償却費"+str(dep)+"/減価償却累計額"+str(dep))

print("（BS　減価償却累計額:"+str(deptotal)+"）")


print("---------------------------------------")
    </py-script>
  </body>
</html>
