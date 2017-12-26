# accessibility
이 레포지토리는 웹 접근성에 대한 개인적인 가이드라인을 적어놓을 목적으로 만들어졌습니다.

## Rules

### URL의 변경이 없는 경우 `<a>`를 사용하지 않습니다. 불가피하게 사용해야 한다면 `role` 속성을 명시합니다.

**Bad**

``` html
<a href="#" onclick="close()">X</a>
```

**Good**

``` html
<a href="#" role="button" onclick="close()">X</a>
```

**Best**

``` html
<button aria-label="Close" onclick="close()">X</button>
```

### 레이블을 숨기는 것 대신 [`aria-label`](https://www.w3.org/TR/WCAG20-TECHS/ARIA14.html)을 사용합니다.

**Bad**
``` html
<button onclick="close()">X</button>
```

**Good**

``` html
<button onclick="close()">
  X
  <span style="position: absolute; top: -9999px; left: -9999px;">Close</span>
</button>
```

**Best**

``` html
<button aria-label="Close" onclick="close()">X</button>
```

### 시간 정보를 위해서 `<time>` 요소와 `datetime` 속성을 사용합니다.

**Bad**

``` html
<span>18 hours ago</span>
```

**Good**

``` html
<time datetime="2017-10-30T07:17:04Z">18 hours ago</time>
```

**Best**

``` html
<time datetime="2017-10-30T07:17:04Z" title="Oct 30, 2017 04:17 PM">18 hours ago</time>
```

### 모든 이미지에 `alt` 텍스트를 적용합니다. ([더 읽기](https://moz.com/learn/seo/alt-text))

**Bad**

``` html
<img src="/IronMan/mark-3.jpg"/>
```

**Good**

``` html
<img src="/IronMan/mark-3.jpg" alt="Iron man, mark 3"/>
```

## References

- [10 guidelines to improve your web accessibility](https://aerolab.co/blog/web-accessibility/)
- [Using the button role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_button_role)
