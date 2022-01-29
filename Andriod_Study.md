[TOC]

# Andriod学习

## 前置

### 一、常用辅助网站

#### 1、RGB拾色器网站

​	福步：https://link.fobshanghai.com/rgbcolor.htm

#### 2、图标网站

​	阿里巴巴免费的icon网站iconfont：https://www.iconfont.cn/

#### 3、视频源码网址

​	github：https://github.com/taifus/Android_Learning

## 第一章  文件内容

### 一、后端（Java）

#### 1、主文件

路径：app/src/main/java/(具体的包)/MainActivity

重要生命周期方法onCreate通过setContentView方法声明了布局即Activity_main

### 二、前端（页面）

#### 1、主布局

路径：app/src/main/res/layout/activity_main.xml

### 三、资源文件

#### 1、drawable

路径：app/src/main/res/drawable

内容：图片和自定义的xml文件

#### 2、mipmap

路径：app/src/main/res/mipmap-hdpi、app/src/main/res/mipmap-mdpi、app/src/main/res/mipmap-xhdpi、app/src/main/res/mipmap-xxhdpi、app/src/main/res/mipmap-xxxhdpi

内容：logo

#### 3、values

路径：app/src/main/res/values

内容：颜色（colors）、文字（strings）、样式（styles）

### 四、配置文件

#### 1、AndroidMainfest.xml

路径：app/src/main/AndroidMainfest.xml

内容：应用中所有用到的activitys都需要在这个文件中声明

将Mainactivity设置为启动的activity

![image-20210103123556219](Andriod_Study.assets/image-20210103123556219.png)

#### 2、build.gradle

路径：app/src/build.gradle

内容：android{···

​							compileSdkVersion 编译sdk的版本

​							buildToolsVersion编译工具的版本

​							defaultConfig{  ···

​														versionCode版本号

​														versionName版本名称

​													}

​							}

​			dependencies{···

​							compile ‘xxx’ 使用到的包

​							}

## 第二章  布局

### 一、线性布局LinearLayout

#### 1、常用属性

![image-20210103120150492](Andriod_Study.assets/image-20210103120150492.png)

##### 1.1  android:id

​	线性控件的标志，用来寻找这个控件

​	@+id创建一个id

![image-20210103123720158](Andriod_Study.assets/image-20210103123720158.png)

##### 1.2  andriod:layout_width

​	线性控件的宽度，单位使用dp，不用px（适配不同机型）

​	wrap_content  包含内容，内容有多少，宽度就为多少

​	match_parent  匹配父控件，父控件有多少，宽度就为多少

##### 1.3  andriod:layout_height

​	线性控件的高度，单位使用dp（字体使用sp）不用px（适配不同机型）

​	wrap_content  包含内容，内容有多少，宽度就为多少

​	match_parent  匹配父控件，父控件有多少，宽度就为多少

##### 1.4  andriod:background

​	线性控件的背景，颜色、图片和自定义的xml文件

​	#000000  黑色	//fobshanghai.com/rgbcolor.htm取色

##### 1.5  andriod:layout_margin

​	线性控件的外边距，单位使用dp（字体使用sp）不用px（适配不同机型）

##### 1.6  andriod:layout_padding

​	线性控件的内边距，单位使用dp（字体使用sp）不用px（适配不同机型）

![image-20210103124929758](Andriod_Study.assets/image-20210103124929758.png)

##### 1.7  andriod:orientation

​	线性控件的方向，默认为水平

​	vertical  垂直方向

​	horizontal  水平方向

##### 1.8  andriod:gravity

​	对齐方式（内部元素排列方式）

​	bootm  底部对齐

​	right  右部对齐

​	left  左部对齐

​	top  上部对齐

​	center  居中对齐

​	center_horizontal  水平居中

​	center_vertical  垂直居中

##### 1.9  andriod:layout_weight

​	减掉父控件被占用的空间后剩余部分根据权重划分

#### 2、View

**所有控件的父类**

### 二、相对布局RelativeLayout

#### 1、最常用属性

![image-20210103131824068](Andriod_Study.assets/image-20210103131824068.png)

##### 1.1  android:layout_toLeftOf

​	在某个控件的左边

##### 1.2  android:layout_toRightOf

​	在某个控件的右边

##### 1.3  android:layout_alignBootom

​	跟某个控件底部对齐

##### 1.4  android:layout_alignParentBootom

​	跟父控件底部对齐

##### 1.5  android:layout_below

​	在某个控件的下边

### 三、文字布局TextView

#### 1、最常用属性

![image-20210103131743407](Andriod_Study.assets/image-20210103131743407.png)

##### 1.1  文字大小、颜色

​	文字内容：android:text  //可以引用字符串，也可以直接写文字

​	文字显示为大写：android:textAllCaps="true"  //默认为true

​	文字颜色：android:textColor

​	文字大小：android:textSize  //字体大小使用sp

##### 1.2  显示不下使用...

​	文字行数：android:maxLines

​	使用...：android:ellipsize="end"

##### 1.3  文字+icon

​	图片放在drawable文件夹下

![image-20210103134204951](Andriod_Study.assets/image-20210103134204951.png)

![image-20210103134352576](Andriod_Study.assets/image-20210103134352576.png)

##### 1.4  中划线、下划线

​	中划线

![image-20210103134728904](Andriod_Study.assets/image-20210103134728904.png)![image-20210103

​	下划线

![image-20210103134829922](Andriod_Study.assets/image-20210103134829922.png)

​	//通过html设置下划线

![image-20210103135023406](Andriod_Study.assets/image-20210103135023406.png)

##### 1.5  跑马灯

​	文字行数：android:singlLine=“true”

​	使用跑马灯：android:ellipsize="marquee"

​	跑马灯重复次数：android:marqueeRepeatLimit=“marquee_forever”  //一直重复，也可以写成-1

​	获取焦点：android:focusable=“true”

​	焦点被触及：android:focusableInTouchMode=“true”

#### 2、Button

​	为TextView的子类

##### 2.1  最主要属性

![image-20210103140100226](Andriod_Study.assets/image-20210103140100226.png)

![image-20210103132528310](Andriod_Study.assets/image-20210103132528310.png)

##### 2.2  在activity文件中声明button

​	![image-20210103132641699](Andriod_Study.assets/image-20210103132641699.png)

##### 2.3  在activity文件中找到button

​	findViewById返回值为View，需要强制类型转换为子类Button

![image-20210103132743408](Andriod_Study.assets/image-20210103132743408.png)

##### 2.4  在activity文件中设置button点击事件

![image-20210103132928313](Andriod_Study.assets/image-20210103132928313.png)

##### 2.5  新建一个activity

![image-20210103133032425](Andriod_Study.assets/image-20210103133032425.png)

​	在AndroidMainfest.xml中声明activity，‘.’代表包名

![image-20210103133143903](Andriod_Study.assets/image-20210103133143903.png)

##### 2.6  跳转到新创建的activity

![image-20210103133321670](Andriod_Study.assets/image-20210103133321670.png)

##### 2.7  添加背景，使button显示为圆角

![image-20210103141010253](Andriod_Study.assets/image-20210103141010253.png)

##### 2.8  添加背景，使button显示描边

![image-20210103141308592](Andriod_Study.assets/image-20210103141308592.png)

##### 2.9  添加背景，是button出现按压效果

![image-20210103141631767](Andriod_Study.assets/image-20210103141631767.png)

##### 2.9  设置点击事件

1、android:onClick=“showToast”

​	在activity中设置函数showToast

![image-20210103142132045](Andriod_Study.assets/image-20210103142132045.png)

2、直接在activity中设置点击事件

![image-20210103142341459](Andriod_Study.assets/image-20210103142341459.png)

#### 3、EditText

​	TextView的子类

![image-20210103143037978](Andriod_Study.assets/image-20210103143037978.png)

##### 3.1  主要属性

​	提示：android:hint  //默认提示

​	密码不显示：android:inputType="testPassword"

​	数字：android:inputType="number"

##### 3.2  用户名输入框

![image-20210103144523694](Andriod_Study.assets/image-20210103144523694.png)

##### 3.3  密码输入框

![image-20210103144604650](Andriod_Study.assets/image-20210103144604650.png)

##### 3.4  登录按钮

![image-20210103144625775](Andriod_Study.assets/image-20210103144625775.png)

##### 3.5  点击事件

![image-20210103144749616](Andriod_Study.assets/image-20210103144749616.png)

##### 3.6  监听输入文字改变事件

​	addTextChangedListener函数的参数TextWacher包含三个方法，分别是文字改变前，文字改变时和文字改变后

![image-20210103145041469](Andriod_Study.assets/image-20210103145041469.png)

#### 4、RadioButton

![image-20210105143022456](Andriod_Study.assets/image-20210105143022456.png)

##### 4.1  实现button选择跳转

![image-20210105143521738](Andriod_Study.assets/image-20210105143521738.png)

##### 4.2  实现单选

​	在RadioGroup中放置RadioButton，默认选中android:checked=“true”，设置checked属性必须给每个RadioButton一个id属性

![image-20210105144046369](Andriod_Study.assets/image-20210105144046369.png)

##### 4.3  更换样式

​	去掉圆圈，使用android:button="@null"

​	更换背景，根据state_checked设置不同的样式，选中填充，未选中描边

![image-20210105144823596](Andriod_Study.assets/image-20210105144823596.png)

##### 4.4  监听事件

​	监听选中事件，在onCheckedChanged函数中编写选中后执行的内容

![image-20210105145035633](Andriod_Study.assets/image-20210105145035633.png)

#### 5、CheckBox

![image-20210105145224129](Andriod_Study.assets/image-20210105145224129.png)

##### 5.1  实现多选

![image-20210105145618648](Andriod_Study.assets/image-20210105145618648.png)

##### 5.2  自定义选择框

![image-20210105150018779](Andriod_Study.assets/image-20210105150018779.png)

![image-20210105145951959](Andriod_Study.assets/image-20210105145951959.png)

##### 5.3  监听事件

![image-20210105150226292](Andriod_Study.assets/image-20210105150226292.png)

### 四、ImageView

![image-20210105150254915](Andriod_Study.assets/image-20210105150254915.png)

#### 1、主要属性

​	src  图片属性

​	scaleType  缩放类型 fitXY撑满控件

![image-20210105150638269](Andriod_Study.assets/image-20210105150638269.png)

#### 2、加载网络图片

​	第三方库**glide**

![image-20210105151111722](Andriod_Study.assets/image-20210105151111722.png)

![image-20210105151144464](Andriod_Study.assets/image-20210105151144464.png)

​	具体使用

![image-20210105151310384](Andriod_Study.assets/image-20210105151310384.png)

​	申请网络权限  AndroidMainfest.xml

![image-20210105151347247](Andriod_Study.assets/image-20210105151347247.png)

### 五、ListView

![image-20210105151519675](Andriod_Study.assets/image-20210105151519675.png)

##### 1、创建ListViewActivity

![image-20210105151819722](Andriod_Study.assets/image-20210105151819722.png)

#### 2、添加展示页面

![image-20210105151939704](Andriod_Study.assets/image-20210105151939704.png)

![image-20210105151955648](Andriod_Study.assets/image-20210105151955648.png)

#### 3、创建Adapter类

![image-20210105152038200](Andriod_Study.assets/image-20210105152038200.png)

#### 4、展示列表

​	getCount返回值为列表的数量

![image-20210105152251362](Andriod_Study.assets/image-20210105152251362.png)

#### 5、构造布局

![image-20210105152724672](Andriod_Study.assets/image-20210105152724672.png)

#### 6、构造静态类保存布局控件

![image-20210105152905535](Andriod_Study.assets/image-20210105152905535.png)

#### 7、getView函数中设置列表块内容

![image-20210105153032314](Andriod_Study.assets/image-20210105153032314.png)

#### 8、ListViewActivity类中获取展示内容

![image-20210105153124213](Andriod_Study.assets/image-20210105153124213.png)

#### 9、设置网格线

![image-20210105153328274](Andriod_Study.assets/image-20210105153328274.png)

#### 10、点击事件和长点击事件

![image-20210105153458987](Andriod_Study.assets/image-20210105153458987.png)

### 六、GridView

![image-20210105153611431](Andriod_Study.assets/image-20210105153611431.png)

#### 1、主要属性

​	**numColumns** 行数

​	**horizontalSpacing**  行之间的间距

​	**verticalSpacing**  列之间的间距

![image-20210105153904029](Andriod_Study.assets/image-20210105153904029.png)

#### 2、设置展示内容

![image-20210105154731899](Andriod_Study.assets/image-20210105154731899.png)

#### 3、点击事件和长点击事件

![image-20210105154621310](Andriod_Study.assets/image-20210105154621310.png)

### 七、滚动视图ScrollView

![image-20210105154914060](Andriod_Study.assets/image-20210105154914060.png)

#### 1、属性

​	子视图只能有一个，可以在需要滚动的视图外加一个ScrollView

![image-20210105155148326](Andriod_Study.assets/image-20210105155148326.png)

#### 2、水平滚动

![image-20210105155407178](Andriod_Study.assets/image-20210105155407178.png)

### 八、RecyclerView

#### 1、主要特点

![image-20210105155504767](Andriod_Study.assets/image-20210105155504767.png)

![image-20210105155619112](Andriod_Study.assets/image-20210105155619112.png)

##### 1.1  需要的库

![image-20210105155658347](Andriod_Study.assets/image-20210105155658347.png)

#### 2、实现Adapter

![image-20210120141450968](Andriod_Study.assets/image-20210120141450968.png)

![image-20210105160252342](Andriod_Study.assets/image-20210105160252342.png)

![image-20210105160536168](Andriod_Study.assets/image-20210105160536168.png)

![image-20210105160654769](Andriod_Study.assets/image-20210105160654769.png)

![image-20210105160616289](Andriod_Study.assets/image-20210105160616289.png)

#### 3、获取展示内容

![image-20210105160836838](Andriod_Study.assets/image-20210105160836838.png)

#### 4、添加分割线

![image-20210105161320067](Andriod_Study.assets/image-20210105161320067.png)

##### 4.1  添加dimen

![image-20210105161512804](Andriod_Study.assets/image-20210105161512804.png)

##### 4.2  实现类

![image-20210105161259420](Andriod_Study.assets/image-20210105161259420.png)

#### 5、监听点击事件

![image-20210105161845609](Andriod_Study.assets/image-20210105161845609.png)

##### 5.1  可以通过回调方法实现与其他视图一样的监听方式

![image-20210105162144544](Andriod_Study.assets/image-20210105162144544.png)

![image-20210105162223038](Andriod_Study.assets/image-20210105162223038.png)

![image-20210105162053750](Andriod_Study.assets/image-20210105162053750.png)

![image-20210105162012024](Andriod_Study.assets/image-20210105162012024.png)

#### 6、水平展示

![image-20210105162820836](Andriod_Study.assets/image-20210105162820836.png)

#### 7、网格展示

​	gridLayoutManager的第二个参数为分成几列

![image-20210105163439218](Andriod_Study.assets/image-20210105163439218.png)

#### 8、瀑布流

​	StaggeredGridLayoutManager的第一个参数为行数或列数

![image-20210105163927466](Andriod_Study.assets/image-20210105163927466.png)

​	**加载图片**

![image-20210105164102336](Andriod_Study.assets/image-20210105164102336.png)

#### 9、ViewHolder

![image-20210105164447815](Andriod_Study.assets/image-20210105164447815.png)

​	**重写onCreateViewHolder方法**

​	返回类型更改为所有视图类型的父类

![image-20210105164855920](Andriod_Study.assets/image-20210105164855920.png)

### 九、WebView网络视图

#### 1、加载网页

![image-20210105170255027](Andriod_Study.assets/image-20210105170255027.png)

##### 1.1  加载url

<img src="Andriod_Study.assets/image-20210105170304691.png" alt="image-20210105170304691" style="zoom: 50%;" />

<img src="Andriod_Study.assets/image-20210105170313092.png" alt="image-20210105170313092" style="zoom: 50%;" />

##### 1.2  加载html代码

<img src="Andriod_Study.assets/image-20210105170332806.png" alt="image-20210105170332806" style="zoom: 50%;" />

##### 1.3  Native和JavaScript互相调用

#### 2、网页的前进后退

<img src="Andriod_Study.assets/image-20210105170510110.png" alt="image-20210105170510110" style="zoom: 67%;" />

![image-20210105170649990](Andriod_Study.assets/image-20210105170649990.png)

#### 3、使用WebView

![image-20210105171030224](Andriod_Study.assets/image-20210105171030224.png)

##### 3.1  加载本地html

![image-20210105170914920](Andriod_Study.assets/image-20210105170914920.png)

##### 3.2  加载网络url

![image-20210105171108713](Andriod_Study.assets/image-20210105171108713.png)

##### 3.3  内部加载url，继续访问

![image-20210109204358014](Andriod_Study.assets/image-20210109204358014.png)

##### 3.4  开始和结束函数  

![image-20210109204445549](Andriod_Study.assets/image-20210109204445549.png)

##### 3.5  更改返回

![image-20210109204635588](Andriod_Study.assets/image-20210109204635588.png)

##### 3.6  进度条和title

![image-20210109205101088](Andriod_Study.assets/image-20210109205101088.png)

##### 3.7  执行js代码

![image-20210109205246827](Andriod_Study.assets/image-20210109205246827.png)

### 十、弹出框

#### 1、Toast

### 十一、Activity

![image-20210109205829826](Andriod_Study.assets/image-20210109205829826.png)

