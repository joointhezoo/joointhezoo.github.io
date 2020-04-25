---
layout: post
title: "불필요한 div를 생성하지 않는 방법"
description: "fragment 관련 지식"
comments: true
keywords: "react, fragment"
---
## Problem

React Component를 생성하다보면 로직으로 돔을 생성하거나 하는경우 (?) 그 돔을 기본적으로 감싸는 엘리먼트가 필요해서 쓸데없이 div를 생성한 케이스가 있었다.


## Solution

이러한 현상을 방지하기 위해 불필요한 div나 돔 엘리먼트를 생성하지 않기 위해 할 수 있는 방법.


1️⃣ Fragment 사용하기

~~~
class case1 extends Component {
    render () {
        <Fragment>
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
        </Fragment>
    }
}
~~~


2️⃣ 함축적인 Fragment 사용하기 

~~~
class case2 extends Component {
    render () {
        <>
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
        </>
    }
}
~~~

3️⃣ Array 형식으로 담기기

~~~
class case3 extends Component {
    render () {
        [
            <div>1</div>,
            <div>2</div>,
            <div>3</div>,
            <div>4</div>
        ]
    }
}
~~~

