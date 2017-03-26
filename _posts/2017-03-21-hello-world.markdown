---
layout: post
title:  "Hello World"
date:   2017-03-21 23:18:28 +0000
categories: git init
---

Made this today to see how well `jekyll` works as a static site generator. May as well keep a blog permanently online if I can just host it on github.

Highlighting appears to be generated at build time, which is nice:

{% highlight rust %}
#[test]
fn mm_multiply() {
    let n = 3;
    let mut a = vec![3.0, 1.0, 1.0, 1.0, 3.0, 1.0, 1.0, 1.0, 3.0];
    let mut w = vec![0.0; n as usize];
    let mut work = vec![0.0; 4 * n as usize];
    let lwork = 4 * n;
    let mut info = 0;

    dsyev(b'V', b'U', n, &mut a, n, &mut w, &mut work, lwork, &mut info);
    assert_eq!(info, 0);

    for (one, another) in w.iter().zip(&[2.0, 2.0, 5.0]) {
        assert!((one - another).abs() < 1e-14);
    }
}
{% endhighlight %}

Maybe I'll just convert the [rust blog][olb-blog] project to this for now. Don't really need a server when this is available.

[old-blog]:   https://github.com/clux/blog
