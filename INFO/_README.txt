
ТЕХСТЕК
------------
Spring Web MVC
https://docs.spring.io/spring-framework/reference/web/webmvc.html

Hibernate 6
https://hibernate.org/

MySQL 8
https://www.mysql.com/

Bootstrap 5
https://getbootstrap.com/
https://getbootstrap.com/docs/5.3/getting-started/introduction/
https://getbootstrap.com/docs/5.3/extend/icons/

Vector icons & stickers
https://www.flaticon.com/

Favicon Generator
https://favicon.io/favicon-converter/

Pixabay
https://pixabay.com/


---------------------------------------------------------------------

1) Складаємо SQL-запити INFO/SQLs.sql

2) Створюємо Maven-проект.
В Advanced Settings можемо прописати org.example.app

3) Додаємо залежності в pom.xml

4) У корені проекту створемо папку Сatalina,
де мають бути сгенеровані відповідні файли.
Catalina – контейнер сервлетів Apache Tomcat.
Catalina реалізує специфікації для сервлета та JSP.

5) Формуємо контент в src/main/resources

6) Створюємо src/main/webapp та формуємо контент:
- src/main/webapp/resources: іконки, зображення.
- src/main/webapp/WEB-INF/views: JSP-файли (презентація).

7) Формуємо контент org/example/app

8) Для роботи з сервером у IntelliJ IDEA Community Edition
необхідний плагін.
File > Settings > Plugins > Marketplace.
Знаходимо плагін Smart Tomcat, встановлюємо.

* Якщо IntelliJ IDEA Ultimate, то без плагіна
https://www.jetbrains.com/help/idea/developing-web-applications.html

9) Конфігуруємо Smart Tomcat.

Run > Edit Configurations... > + > Smart Tomcat

Вкладка Configuration.

В Name пишемо, наприклад, spring-mvc-jsp.

Клікаємо Configure. Стаємо на Tomcat Server. Клікаємо + .
Вибираємо папку необхідного Apache Tomcat.
Краще вибрати сервер, який встановлений із zip-файлу,
оскільки не вимагає зайвої аутентифікації при запуску.

Клікаємо OK.

Catalina base.
Вказуємо шлях до нашої папки Catalina.

Deployment directory.
Вибираємо папку webapp свого проекту.

Use classpath of module має містити найменування
кореневої папки проекту.

Context path.
Можна прописати /spring-mvc-jsp або просто /

Server port повинен містити порт Apache Tomcat, який
в налаштуваннях сервера.
Див. на сервері /conf/server.xml
<Connector port="8080"...

Клікаємо Apply та OK.

10) Запустимо Tomcat.
В IDE, зверху, клікаємо зелену кнопку запуску.
В консолі мають з'явитись повідомлення про функціонування
сервера.
Зупинити сервер можна, натиснувши червоний квадратик вгорі,
який має з'явитися після запуску сервера.

11) Сформуємо jar-файл (опційно).
Клікаємо праворуч Maven. Відкривається панель Maven.
В Lyfecycle клікаємо послідовно clean, compile, package.
В панель_проекта/target має з'явитися jar-файл.
Цей jar-файл копіюємо до папки webapps сервера на локальній машині.

12) Перевіряємо працездатність програми.
Запускаємо сервер.
В консолі повинно з'явитися таке посилання
http://localhost:8080/
або, якщо, попередньо прописали /spring-mvc-jsp, то таке
http://localhost:8080/spring-mvc-jsp
Клікаємо на посилання.
В браузері з'явиться стартова сторінка Web-додатку.
Тестуємо функціонал додатку.
Також перевіряємо внесення даних в БД через Workbench.

