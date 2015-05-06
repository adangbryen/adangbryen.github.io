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
    
* 文字记录一下使用过程 

`//默认是migration目录下的文件  `
    
    $php artisan migrate 
    $php artisan help make:migration
    $php artisan make:migration create_customers_table --create="customers"

    this is code

##### this is tilte
    this is code again

{
    这里写代码 看看 {}
}
    
#####产生如下代码 可以开始写自己的代码了
    use Illuminate\Database\Schema\Blueprint;
    use Illuminate\Database\Migrations\Migration;

    class CreateCustomersTable extends Migration {

        /**
         - Run the migrations.
         *
         - @return void
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
         - Reverse the migrations.
         *
         - @return void
         */
        public function down()
        {
            Schema::drop('customers');
        }

    }
#### code code code

    []$ php artisan make:migration add_test_to_customers --table="customers"
    <?php

    use Illuminate\Database\Schema\Blueprint;
    use Illuminate\Database\Migrations\Migration;

    class AddTestToCustomer extends Migration {

        /**
         - Run the migrations.
         *
         - @return void
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
         - Reverse the migrations.
         *
         - @return void
         */
        public function down()
        {
            Schema::table('customers', function(Blueprint $table)
            {
                $table->dropColumn('etea');
            });
        }

    }

'cd ~\Library\Performance\webide80\colors`

<!--break-->
