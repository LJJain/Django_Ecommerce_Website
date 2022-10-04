# Django Ecommerce Website

## Github

> git remote add origin https://github.com/LJJain/Django_Ecommerce_Website.git

## 日誌

> 2022.10.02

    - 建立專案(ecommerce) & 新增app(store)
    - 建立靜態文件
    - 導入 Bootstrap & 繼承main.html 模板
    - store.html 建置

> 2022.10.03

    - 建立模組 models.py
    - 商品展示 & 購物車功能 & 結帳 (修改views.py & html)

> 2022.10.04

    - 添加功能邏輯
    - 訪客購物車資訊 -> 利用cookie
    - 建立 支付功能 (paypalapi)

## 筆記

> 建立專案(ecommerce) & 新增 app(store)

    - 建立專案: django-admin startproject ecommerce .
    - 新增app(store): python manage.py startapp store
    - root/settings.py: INSTALLED_APPS = ['store.apps.StoreConfig',]
    - store/:新增 templates/store 資料夾
    - store/templates/store: 新增 main、store、cart、checkout.html
    - 修改views.py
    - store/:新增 urls.py 並建立path & root/urls.py: 新增 include path
    - python manage.py runserver

> 建立靜態文件

    - root/: 新增 static資料夾/ css、 images 資料夾
    - settings.py: STATICFILES_DIRS = [os.path.join( BASE_DIR, 'static')] (import os)
    - 修改 html & 載入圖片 (jinja2 語法)
    - 修改 main.html 載入 mani.css

> Bootstrap

    - source code: https://github.com/divanov11/ecom_steps/blob/master/prt5_stp3_main.html
    - main.html添加 Navbar、contant
    - 繼承 main.html 模板 : store、checkout、cart.html
    - 引入 Navbar(Bootstap) source code: https://getbootstrap.com/docs/4.0/components/navbar/#supported-content

> 建立模組 models.py

    - 設定需要的模組表單 models.py
    - python manag.py makemigrations (terminal)
    - python manage.py migrate (terminal)
    - 註冊models: admin.py
    - 新增 superuser : python manage.py createsuperuser -> python manage.py runserver (確定表單是否建立完成)

> 新增產品

    - 產品照片先不要放進static資料夾
    - pip install pillow (python 圖片庫)
    - 建立 MEDIA_ROOT = os.path.join(BASE_DIR, 'static/images') (settings.py)
    - 上傳照片: 測試是否會自動傳入images資料夾裡
    - MEDIA_URL = '/images/' (settings.py)
    - 修改root/urls.py

> 加入購物車功能製作

    - 建立 js/cart.js
    - main.html 載入 carts.js
    - https://www.youtube.com/watch?v=woORrr3QNh8&list=PL-51WBLyFTg0omnamUjL1TCVov7yDTRng&index=5&t=920s&ab_channel=DennisIvy

> 訪客購物車資訊

    - https://www.youtube.com/watch?v=kH2FOWuA4uI&list=PL-51WBLyFTg0omnamUjL1TCVov7yDTRng&index=5&ab_channel=DennisIvy
    - 獲取cookie (js) : function getCookie(name){} -> main.html
    - js邏輯修改 (cart.js) & views.py

> 重複代碼 繼承(utils.py)

    - D.R.Y(Don't Repeat Yourself)技術

> 支付功能 (paypal)

    - button code: https://developer.paypal.com/demo/checkout/#/pattern/client
    - button style: https://developer.paypal.com/docs/archive/checkout/how-to/customize-button/#supported-locales

## 參考資料

    - https://codewithsteps.herokuapp.com/
    - Html特殊符號: https://www.toptal.com/designers/htmlarrows/
