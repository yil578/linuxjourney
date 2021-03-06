# arp

## محتوای درس

حتما به یاد می‌آورید که وقتی آدرس MAC مورد نظر را با ARP جستجو می‌کنیم‌، این دستور
اول کش ذخیره شده اش روی سیستم ما را بررسی می‌کند. در واقع شما می‌توانید این دستور
را امتحان کنید:


```
pete@icebox:~$ arp
Address                  HWtype  HWaddress           Flags Mask            Iface
192.168.22.1            ether   00:12:24:fc:12:cc   C                     eth0
192.168.22.254          ether   00:12:45:f2:84:64   C                     eth0
```

این کش در زمان بارگذاری سیستم خالی است و هنگام ارسال بسته‌های شبکه به میزبان‌های
دیگر‌، ساخته می‌شود. اگر ما بسته‌ای را به مقصدی که در کش ARP موجود نیست ارسال کنیم‌،
مراحل زیر رخ می‌دهند:

- هاست مبدا یک قالب اترنت به همراه بستهٔ درخواستی ایجاد می‌کند.
- هاست مبدا بستهٔ تولید شده را به کل شبکه ارسال می‌کند.
- اگر هاستی روی شبکه آدرس MAC درست را بداند‌، بستهٔ پاسخی شامل آدرس MAC را به هاست
  میزبان بر می‌گرداند.
- هاست مبدا شناسهٔ IP و آدرس MAC هاست پاسخ دهنده را در کش ARP ذخیره کرده و سپس به
  ادامهٔ ارسال بسته می‌پردازد.
  
همچنین شما می‌توانید کش ARP سیستم خود را با دستور `ip` نیز مشاهده کنید:

```
$ ip neighbour show
```

## تمرینات

بررسی کنید که زمانی بارگذاری مجدد سیستم و یا اعمال عملیاتی روی شبکه‌، چه تغییری در کش ARP سیستم‌تان رخ می‌دهد. 

## سوال آزمون

از کدام دستور می‌توانید برای مشاهدهٔ کش ARP سیستم‌تان استفاده کنید؟

## پاسخ آزمون

arp
