# 导航

## 配置

### 标题

```php
    /**
     * The component display name
     *
     * @var string
     */
    protected $title;
```


### 图标

```php
    /**
     * The page icon class name.
     *
     * @var string|null
     */
    protected $icon;
```
图标的class名，如：`fa-user`


### 页面ID

```php
    /**
     * The page id name.
     *
     * @var string|null
     */
    protected $pageId;
```

### 页面从属的父级页面ID

```php
    /**
     * The page belong to page id name.
     *
     * @var string
     */
    protected $parentPageId;
```
> 父级页面一般只是一个分组，无实际访问页面

### 权重

```php
    /**
     * The page priority.
     *
     * @var int
     */
    protected $priority = 100;
```
值越小排名越靠前