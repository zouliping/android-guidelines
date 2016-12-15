### 类命名规范

类名采用大驼峰命名法，尽量避免缩写，带上组件名后缀，例如 `SplashActivity`，`UserFragment`，`DownloadService` 等。

### 方法名命名规范

方法名采用小驼峰命名法，使用动词或动名词，例如 `initView()`，`getUserId()`，`updateContent()`，`loadData()` 等。

### 变量命名规范

变量分为成员变量、常量和静态变量。

#### 成员变量

成员变量使用小驼峰命名法。其中 private 和 protected 的非静态成员变量以 m 开头，例如 mUserId。对于 View 变量的命名，以其对应 View 的缩写开头，例如 `tvUserName`，`btnLogin` 等。

#### 常量

常量使用全大写字母命名，中间使用下划线分割，例如 `KEY_SEARCH_KEYWORD`。 

#### 静态变量

静态变量以 s 开头，例如 `sOpenId`。

#### 变量的排列顺序

变量的排序可以按照以下顺序：

1. 常量。常量按照使用先后排列。
2. UI 组件。UI 组件以在布局文件中出现的顺序排列。
3. 普通常量 。普通常量按照使用先后排列。

### 资源文件命名规范

所有资源全部小写，以下划线分割，以下内容不重复此要求。

#### Layout 命名规范

Layout 以组件类型开头，例如 `activity_main`，`view_share`，`item_user` 等。

#### 控件 id 命名规范

控件 id 以 `页面名_内容_控件类型缩写` 为格式，例如 `item_user_avatar_iv` 等。

#### String 资源命名规范

String 以说明该 String 含义的英文释义为命名，例如 `my_follower`对应`我的关注者`。

#### Color 资源命名规范

Color 以 color 开头，下划线后接颜色值的 16 进制，例如 `color_b5b5b5`。

#### Drawable 资源命名规范

图标的命名一般由设计师完成，可以和设计师协商。单个图标可以以 `ic` 开头，背景图片可以以 `bg` 开头。如果图标包含状态，可以以 `pressed`，`selected`，`focused` 等结尾。

#### 动画文件命名规范

动画以 `动画类型_动画方向` 为格式，例如 `fade_in`，`push_left_in` 等。

### 注释规范

注释使用 `/****/` 和 `//` 均可，尽可能在逻辑复杂的地方加上清晰明了的注释。

### 空格的使用

用 4 个空格缩进块。用 8 个空格换行，包括函数调用和赋值。例如，下面的这个例子是正确的：

```
Instrument i =
        someLongExpression(that, wouldNotFit, on, one, line);
```
而下面这个例子就是错误的：

```
Instrument i =
    someLongExpression(that, wouldNotFit, on, one, line);
```

### 大括号的使用

左大括号与代码间隔一个空格，不需重起一行，右大括号可单独一行。此外，如果大括号间只有一行语句，也写上大括号，不要省略。例如：

```
private void init() {
    hello()
}
```

### 代码的长度

一行代码不要过长，尽可能保持在 100 字符以内。一个方法也不要过长，尽可能保持在 50 行以内。