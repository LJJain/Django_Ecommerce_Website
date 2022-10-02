# Django Ecommerce Website

## Github

> git remote add origin https://github.com/LJJain/Django_Ecommerce_Website.git

## 日誌

> 2022.10.02

    - 建立專案(ecommerce) & 新增app(store)
    - 建立靜態文件
    - 導入 Bootstrap & 繼承main.html 模板
    - store.html 建置

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

> 修改 store.html

    -

## 參考資料

    - https://codewithsteps.herokuapp.com/
    - Html特殊符號: https://www.toptal.com/designers/htmlarrows/
