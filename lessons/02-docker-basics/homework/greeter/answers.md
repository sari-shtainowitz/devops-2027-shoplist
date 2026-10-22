1.docker build -t greeter:v1 lessons/02-docker-basics/homework/greeter
2.docker run -d --name greeter -p 9000:8000 greeter:v1
3.docker run -d --name greeter -p 9000:8000 -e GREETING=Shalom greeter:v1
4.{"message": "Shalom, Rivka!"}
5.רק קובץ app.py ירוץ מחדש כי שם יש את השינו בקוד כול שאר הקבצים והתלויות הם לא צריכים שינוי כי נמצאים לפני השינוי
