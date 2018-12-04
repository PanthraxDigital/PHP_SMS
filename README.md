
## Installation and use
# SMS is build using Laravel 4.2
```
$ git clone https://github.com/PanthraxDigital/PHP_SMS.git
```
```
$ cd school-management-system
```

**Change configuration according your need and create Database**
```
$ composer install
```
```
$ php artisan migrate
```
```
$ php artisan db:seed
```
```
$ php artisan serve
```
**  http://localhost:8000 **
USER: admin
PASS: demo123


:information_desk_person:
**About SMS Sending**
- If you configure api link [here](https://github.com/PanthraxDigital/school-management-system/blob/master/app/controllers/attendanceController.php#L221) then sms will be send to the number.
- If you want to send bulk sms from the menu you have to congifure api link
    also in [here](https://github.com/PanthraxDigital/school-management-system/blob/master/app/controllers/smsController.php#L179). Bulk sms will not send currently it store in queue inside the database
    so you have process that queue. For that you can set a cron job with below command:
    ```
    php artisan queue:listen
    ```
