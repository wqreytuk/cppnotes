# 语法

union
所谓超级变量，用到哪个类型就占用哪个类型字节数量，可以用于节省内存空间
比如说结构体中有一个字段，无法确定应该使用哪个类型，可能是多个类型中的任意一种
如果不适用union，你可能需要给每一个类型在结构体中定义一个字段，如果使用了union
你就只需要定义一个字段，里面写上所有候选类型即可


accert
在包含cassert之前定义宏`NDEBUG`可以让assert()失效


函数指针的解释
观察这个语句`void (*funcPtr)();`
解析的规则为，从中间看，看到funcPtr，此时就解释为`funcPtr`是一个。。。。，往右看，碰到右括号，然后往左看，看到`*`，解释为funcPtr是一个指针，指向。。。。
往右看，看到一对括号，解释为funcPtr是一个指向接受空参数的函数的指针
往左看，看到void，解释为funcPtr是一个指向参数列表为空，返回值为void的函数的指针
这里可以看到，`*funcPtr`是被括号括起来的，如果没有把它括起来，编译器就会将其解释为返回值为`void*`的函数


