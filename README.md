# FLASK_SQLALCHEMY_BASICS 
## Creating an environment first ##
 ## Install the python3-venv package ##
  sudo apt install python3.10-venv
 ## Recreate your virtual environment ## 
  python3 -m venv env
 ## Activare the environment ## 
  source env/bin/activate


## Install Libraries ##
 pip install flask flask-sqlalchemy

## Create app.py file ## 
 touch app.py

 ## Create Models ##

 ## Create relationships ##

 ## Create a Database ##
  flask shell
  from app import db
  db.create_all()

  exit()

  ## Opening The Database ##
  sqlite3 db.sqlite3
  cd instance
  .tables
  .schema
## Insert Data ##
   flask shell
   from app import db, product, Order, Customer
   lemuelmaturwe = Customer(
    first_name='Lemuel',
    last_name='Maturwe',
    address='123 Fake Street',
    city='Miami',
    postcode='12345',
    email='lemuelmaturwe@gmail.com'
)
 
 db.session.add(lemuelmaturwe)
 db.session.commit()
 exit()
 sqlite3 db.sqlite3
 select * from customer;
 .exit
  ## create a product ##
  flask shell
  from app import db, Customer, Order, product
  computer = product(name='computer', price=80)
  db.session.add(computer)
  db.session.commit()
  phone = product(name='Phone', price=20)
  db.session.add(Phone)
  db.session.commit()

  ## creating an order ##
  order = Order(
    coupon_code='FREESHIPPING',
    customer_id=1,
    products=[computer, phone]
)
db.session.add(order)
db.session.commit()
exit()
cd instance
sqlite3 db.sqlite3
select * from product;

## update Data ##
from app import db, Customer
lemuelmaturwe = Customer.query.filter_by(id=1).first()
lemuelmaturwe.first_name
lemuelmaturwe.last_name
lemuelmaturwe.address
lemuelmaturwe.address = '456 Fake Street'
db.session.commit()

## delete data ##
flask shell
from app import db, Customer

ashley = Customer(first_name='Ashley', last_name='smith', address='123 Fake Street', city='Miami', postcode='12345', email='ashley@gmail.com')

db.session.add(ashley)
db.session.commit()