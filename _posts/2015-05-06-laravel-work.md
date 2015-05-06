---  
layout: post
title: "laravel 使用记录"
description: "laravel 使用记录"
category: phpstorm
tags: [phpstorm, php]
---
{% include JB/setup %}
# laravel 使用习惯
---

 
**参考 [视频连接](https://laracasts.com/series/)**
####laravel 使用记录 
> 数据库 migrate 使用 [https://laracasts.com/](https://laracasts.com/series/laravel-5-fundamentals/episodes/7)
> 
* 文字记录一下使用过程 

```
//默认是migration目录下的文件php artisan migrate 
php artisan help make:migration
php artisan make:migration create_customers_table --create="customers"
<!--break-->

* 产生如下代码 可以开始写自己的代码了

```
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class CreateCustomersTable extends Migration {

    /**
     * Run the migrations.
     *
     * @return void
     */
    public function up()
    {
        Schema::create('customers', function(Blueprint $table)
        {
            $table->increments('id');
            $table->timestamps();
        });
    }

    /**
     * Reverse the migrations.
     *
     * @return void
     */
    public function down()
    {
        Schema::drop('customers');
    }

}
<!--break-->

*-----*
```
[]$ php artisan make:migration add_test_to_customers --table="customers"
<?php

use Illuminate\Database\Schema\Blueprint;
use Illuminate\Database\Migrations\Migration;

class AddTestToCustomer extends Migration {

    /**
     * Run the migrations.
     *
     * @return void
     */
    public function up()
    {
        Schema::table('customers', function(Blueprint $table)
        {
            //$table->increments('');
            //$table->timestamps();
            $table->boolean('etea');
        });
    }

    /**
     * Reverse the migrations.
     *
     * @return void
     */
    public function down()
    {
        Schema::table('customers', function(Blueprint $table)
        {
            $table->dropColumn('etea');
        });
    }

}

```
    cd ~\Library\Performance\webide80\colors
,,,
 wget https://raw.githubusercontent.com/daylerees/colour-schemes/master/jetbrains/earthsong.icls
 下载之后 重启phpstorm  选中刚刚下载的主题
3. color ide  command+shift+a 打开 plugins 输入color 选择color ide install 然后重启
4. 快捷键 command+, * 打开keymaps 修改command+p 为open file的快捷键
                    *command + R   查看本页的结构  --> file structures
                    *command + o 查找symbol 快捷键
    这样下来 常用的>>command + i symbol >>command + o class >>command+p open file(这个跟sublime text保持一致)
5. 保持对齐  command + alt + f  reformat code
6. 自定义对齐格式  > wrappings and braces >> brace placement  >>> class declaration >>>> end of line  
                                                            >>> other >>>> next line  
                > blank lines          -- after class header  --- 1
                > others               -- 


<!--break-->
