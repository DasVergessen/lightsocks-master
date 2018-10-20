规则
----

    文件名必须是 _test.go 结尾的,这样在执行 go test 的时候才会执行对应的代码
    你必须 import test 这个包
    所有的测试用例必须是 Test 开头
    测试用例会按照源码中写的顺序执行
    测试函数 TestXxxx() 的参数是 testing.T, 我们可以使用该类型来记录错误或者是测试状态
    函数中通过调用testing.T的Error, Errorf, FailNow, Fatal, FatalIf方法，说明测试不通过，调用Log方法用来记录测试的信息。
    测试格式：func TestXxx (t *testing.T),Xxx部分可以为任意的字母数字的组合，但是首字母不能是小写字母[a-z]，例如Testintdiv是错误的函数名


说明
----

    ## 单元测试
    go test . 编译当前文件夹所有test测试用例
    go test -v 打印测试信息（默认不打印测试通过信息）

    ## 压力测试


