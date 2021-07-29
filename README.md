ComputerShopitemsale = {
    1: [1,  'laptop',  'Apple Macbook Air',  '$1345',  '$94.15', 'Yes'],
    2: [ 2,  'laptop',  'ASUS S533EQ 15.6',  '$1448', '$101.36','No'],
    3: [3, 'laptop', 'Lenovo IP 3', '$1308', '$91.56', 'No'],
    4: [ 4, 'tablet', 'Samsung 64GB Galaxy TAB', '$372', '$26.04','No'],
    5: [5,  'tablet',  'Apple 10.2-INCH Ipad',  '$456',  '$31.92','Yes'],
    6: [ 6, 'tablet', 'Huawei HW-BAH3 LTE', '$372', '$26.04','Yes'],
    7: [7, 'console',  'Nintendo Switch Console', '$457', '$31.99','Yes'],
    8: [ 8,  'console', 'Sony Playstation 5', '$560', '$39.20','No'],
    9: [ 9,  'console',  'Microsoft Xbox Console', '$653', '$45.71','Yes']}
Userexperience_Shopping = {
    1: {'number': 1, 'category': 'laptop', 'Desc': 'Macbook Air', 'price': 1345, 'Quantity of items': 0,'Memebership': 'N'},
    2: {'number': 2, 'category': 'laptop', 'Desc': 'ASUS 15.6', 'price': 1448, 'Quantity of items': 0,'Memebership': 'N'},
    3: {'number': 3, 'category': 'laptop', 'Desc': 'Lenovo IP 3', 'price': 1308, 'Quantity of items': 0,'Memebership': 'N'},
    4: {'number': 4, 'category': 'tablet', 'Desc': 'Samsung Galaxy TAB', 'price': 372, 'Quantity of items': 0,'Memebership': 'N'},
    5: {'number': 5, 'category': 'tablet', 'Desc': '10.2-INCH Ipad', 'price': 456, 'Quantity of items': 0,'Memebership': 'N'},
    6: {'number': 6, 'category': 'tablet', 'Desc': 'Huawei LTE', 'price': 372, 'Quantity of items': 0,'Memebership': 'N'},
    7: {'number': 7, 'category': 'console', 'Desc': 'Nintendo Switch', 'price': 457, 'Quantity of items': 0,'Memebership': 'N'},
    8: {'number': 8, 'category': 'console', 'Desc': 'Ps5', 'price': 560, 'Quantity of items': 0,'Memebership': 'N'},
    9: {'number': 9, 'category': 'console', 'Desc': 'Xbox', 'price': 653, 'Quantity of items': 0,'Memebership': 'N'}}

def aditionofitems():
 print("{:^30}".format("reference list of items on sale"))
 for i in range(9):
  print("{:^20} | {:^30}".format(i+1,Userexperience_Shopping[1+i]['Desc']))
 Addon = 'Y'
 if Addon == "Y":
   while Addon == 'Y':
    try:
     Item = int(input("Enter the Number:"))
     Quantity = int(input("How many\t"+ Userexperience_Shopping[Item]['Desc'] +"\tdo you want to add to your shoppinglist?:"))
     if Item == 1:
       Userexperience_Shopping[1]['Quantity of items'] = Userexperience_Shopping[1]['Quantity of items'] + Quantity
     elif Item == 2:
       Userexperience_Shopping[2]['Quantity of items'] = Userexperience_Shopping[2]['Quantity of items'] + Quantity
     elif Item == 3:
       Userexperience_Shopping[3]['Quantity of items'] = Userexperience_Shopping[3]['Quantity of items'] + Quantity
     elif Item == 4:
       Userexperience_Shopping[4]['Quantity of items'] = Userexperience_Shopping[4]['Quantity of items'] + Quantity
     elif Item == 5:
       Userexperience_Shopping[5]['Quantity of items'] = Userexperience_Shopping[5]['Quantity of items'] + Quantity
     elif Item == 6:
       Userexperience_Shopping[6]['Quantity of items'] = Userexperience_Shopping[6]['Quantity of items'] + Quantity
     elif Item == 7:
       Userexperience_Shopping[7]['Quantity of items'] = Userexperience_Shopping[7]['Quantity of items'] + Quantity
     elif Item == 8:
       Userexperience_Shopping[8]['Quantity of items'] = Userexperience_Shopping[8]['Quantity of items'] + Quantity
     elif Item == 9:
       Userexperience_Shopping[9]['Quantity of items'] = Userexperience_Shopping[9]['Quantity of items'] + Quantity
    except:
       print("Only numbers not alphabets")
    finally:
       Addon = input("continue adding (Y/N):").upper()
 else:
    print("Return to Menu")

def displayitemsforsale():
    print("%s | %10s | %25s | %5s | %8s | %s" % ("Item Number", "Category", "Names of the Items","Price", "7% Gst","Memebership"),)
    print(("=") * 87)
    for i in range(9):
        print("%11s | %10s | %25s | %5s | %8s | %7s" % (ComputerShopitemsale[i + 1][0],ComputerShopitemsale[i + 1][1],ComputerShopitemsale[i + 1][2],ComputerShopitemsale[i + 1][3],ComputerShopitemsale[i + 1][4],ComputerShopitemsale[i + 1][5]))
        print("=" * 87)
    byprice = input("Do you want to arrange the items by price (Y/N):").upper()
    if byprice == 'Y':
        print("{:^25} | {:^25}".format("Name of Item","Price without gst"))
        print("#="*30)
        for i in range(9):
            print("{:^25} | {:^25}".format(ComputerShopitemsale[i+1][2],ComputerShopitemsale[i+1][3]))
            print("="*60)
def displayordereditems():
  for i in range(9):
   print("{:^20} | {:^30}".format(i+1,Userexperience_Shopping[1+i]['Desc']))
  Again = 'Y'
  while Again == 'Y':
    try:
     Checkup = int(input("Enter the Item you want to check on"))
     if Checkup == 1:
         print(Userexperience_Shopping[1]['Quantity of items'])
     elif Checkup == 2:
         print(Userexperience_Shopping[2]['Quantity of items'])
     elif Checkup == 3:
         print(Userexperience_Shopping[3]['Quantity of items'])
     elif Checkup == 4:
         print(Userexperience_Shopping[4]['Quantity of items'])
     elif Checkup == 5:
         print(Userexperience_Shopping[5]['Quantity of items'])
     elif Checkup == 6:
         print(Userexperience_Shopping[6]['Quantity of items'])
     elif Checkup == 7:
         print(Userexperience_Shopping[7]['Quantity of items'])
     elif Checkup == 8:
         print(Userexperience_Shopping[8]['Quantity of items'])
     elif Checkup == 9:
         print(Userexperience_Shopping[9]['Quantity of items'])
    except:
        print("guys we got a comedic genius here")
        print("But seriously please try again")
    finally:
        Again = input("Do you want to check for another item").upper()

def ControlAltDel():
   Userexperience_Shopping[1]['Quantity of items']=0
   Userexperience_Shopping[2]['Quantity of items']=0
   Userexperience_Shopping[3]['Quantity of items']=0
   Userexperience_Shopping[4]['Quantity of items']=0
   Userexperience_Shopping[5]['Quantity of items']=0
   Userexperience_Shopping[6]['Quantity of items']=0
   Userexperience_Shopping[7]['Quantity of items']=0
   Userexperience_Shopping[8]['Quantity of items']=0
   Userexperience_Shopping[9]['Quantity of items']=0

def Exitprogram():

 memebership = input("Do you have membership(Y/N):").upper()
 Userexperience_Shopping[1]['price']=Userexperience_Shopping[1]['Quantity of items']*Userexperience_Shopping[1]['price']
 Userexperience_Shopping[2]['price']=Userexperience_Shopping[2]['Quantity of items']*Userexperience_Shopping[2]['price']
 Userexperience_Shopping[3]['price']=Userexperience_Shopping[3]['Quantity of items']*Userexperience_Shopping[3]['price']
 Userexperience_Shopping[4]['price']=Userexperience_Shopping[4]['Quantity of items']*Userexperience_Shopping[4]['price']
 Userexperience_Shopping[5]['price']=Userexperience_Shopping[5]['Quantity of items']*Userexperience_Shopping[5]['price']
 Userexperience_Shopping[6]['price']=Userexperience_Shopping[6]['Quantity of items']*Userexperience_Shopping[6]['price']
 Userexperience_Shopping[7]['price']=Userexperience_Shopping[7]['Quantity of items']*Userexperience_Shopping[7]['price']
 Userexperience_Shopping[8]['price']=Userexperience_Shopping[8]['Quantity of items']*Userexperience_Shopping[8]['price']
 Userexperience_Shopping[9]['price']=Userexperience_Shopping[9]['Quantity of items']*Userexperience_Shopping[9]['price']
 if memebership == 'Y':
   Userexperience_Shopping[1]['price']=Userexperience_Shopping[1]['price']*0.9
   Userexperience_Shopping[5]['price']=Userexperience_Shopping[5]['price']*0.9
   Userexperience_Shopping[6]['price']=Userexperience_Shopping[6]['price']*0.9
   Userexperience_Shopping[7]['price']=Userexperience_Shopping[7]['price']*0.9
   Userexperience_Shopping[9]['price']=Userexperience_Shopping[9]['price']*0.9
   Userexperience_Shopping[1]['Memebership']='Y'
   Userexperience_Shopping[5]['Memebership']='Y'
   Userexperience_Shopping[6]['Memebership']='Y'
   Userexperience_Shopping[7]['Memebership']='Y'
   Userexperience_Shopping[9]['Memebership']='Y'
 print("")
 print("{:^90}".format("Your items Ordered"))
 print("{:^90}".format("Thank you and have a nice day ;)"))
 print("#-"*40)
 for i in range(9):
  if Userexperience_Shopping[i+1]['Memebership'] == 'N':
   print("%20s | price sum(excluding gst):\t$ %0.2f" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['price']))
   print("%20s | total price sum(including gst):\t$ %0.2f" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['price']*1.07))
   print("%38s | No.Items:\t %d" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['Quantity of items']))
   print("#-"*40)
  else:
   print("%20s | price (including discount):\t$ %0.2f" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['price']))
   print("%20s | price (excluding discount):\t$ %0.2f" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['price']*100/90))
   print("%20s | total price sum(including gst):\t$ %0.2f" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['price']*1.07))
   print("%38s | No.Items:\t %d" % (Userexperience_Shopping[1+i]['Desc'],Userexperience_Shopping[1+i]['Quantity of items']))
   print("#-"*40)
 print("{:>50} | {:0.2f}".format("The total amount payable",Userexperience_Shopping[1]['price']*1.07+Userexperience_Shopping[2]['price']*1.07+Userexperience_Shopping[3]['price']*1.07+Userexperience_Shopping[4]['price']*1.07+Userexperience_Shopping[5]['price']*1.07+Userexperience_Shopping[6]['price']*1.07+Userexperience_Shopping[7]['price']*1.07+Userexperience_Shopping[8]['price']*1.07+Userexperience_Shopping[9]['price']*1.07))

def MainMenu():
 while True:
    print('{:^40}'.format("~"*30+"Welcome to Consumer Network how can we help you"+"~"*30))
    print('\t''A.view the list of items for sale ')
    print('\t''B.Add items to your shopping list ')
    print('\t''C.Check the items on current list of ordered items ')
    print('\t''D.Clear the shopping list ')
    print('\t''E.I am done peace out')
    selection = input("What is the alphabet you want to make?:").upper()

    if selection == 'A':
        displayitemsforsale()
    elif selection == 'B':
        aditionofitems()
    elif selection == 'C':
        displayordereditems()
    elif selection == 'D':
        ControlAltDel()
    elif selection == 'E':
        Exitprogram()
        break
    else:
        print("Please try again")

MainMenu()
