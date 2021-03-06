# 权限

> `Sco-Admin` 自身并没有继承权限功能，只实现了判断方法，权限的判断逻辑通过观察者模式实现。

## 配置

```php
    /**
     * Access observer class
     *
     * @var string
     */
    protected $observer;
    
    /**
     * User exposed observable abilities.
     *
     * @var array
     */
    protected $observables = [];
```

### observer
指定权限判断的观察者类

### observables 
扩展可用的权限种类
默认的权限种类：display | create | edit | delete | destroy | restore

## 观察者类

### 创建类

命令行执行以下命令:
```php
php artisan make:observer <name>
```
执行后生成如下类，`$component` 是观察者类所在的组件实例。

```php
namespace App\Components\Observers;

use Sco\Admin\Contracts\ComponentInterface;

class PostObserver
{
    public function display(ComponentInterface $component)
    {
        return true;
    }

    public function create(ComponentInterface $component)
    {
        return true;
    }

    public function edit(ComponentInterface $component)
    {
        return true;
    }

    public function delete(ComponentInterface $component)
    {
        return true;
    }

    public function destroy(ComponentInterface $component)
    {
        return true;
    }

    public function restore(ComponentInterface $component)
    {
        return true;
    }
}
```




