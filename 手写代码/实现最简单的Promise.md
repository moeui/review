# 实现最简单Promise



    function MyPromise(fn) {
        let doneCallback
        this.then = function (done) {
            doneCallback = done
        }
        function resolve(res) {
            setTimeout(() => {
                if (doneCallback) doneCallback(res)
            }, 0)
        }
        fn(resolve)
    }

调用:

    const fetch = ()=>{
        return new MyPromise((resolve, reject) => {
        setTimeout(() => {
            resolve(true)
        }, 1000)
    })
    }

    const fn = async () => {
        const b = await fetch()
        console.log(b)
    }
    fn()

- async函数其实是Geneator函数的语法糖。

- then+下一步操作

1.async函数的返回值是Promise对象可以用then方法指定下一步的操作。
2.async函数可以看做多个异步操作，包装成一个Promise对象
3.await命令就是内部then命令的语法糖。

- then+回调函数

1.async函数返回一个Promise对象
2.可以使用then方法添加回调函数。
3.当函数执行的时候，一旦遇到await就会先返回
4.等到异步操作完成，再接着执行函数体后面的语句。
5.async函数内部return语句返回的值，会成为then方法回调函数的参数。