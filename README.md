# accessibility
이 레포지토리는 웹 접근성에 대한 개인적인 가이드라인을 적어놓을 목적으로 만들어졌습니다.

## Rules

### URL의 변경이 없는 경우 `<a>`를 사용하지 않습니다. 불가피하게 사용해야 한다면 `role` 속성을 명시합니다.

**Don't**

``` html
<a href="#" onclick="close()">X</a>
```

**Better**

``` html
<a href="#" role="button" onclick="close()">X</a>
```

**Best**

``` html
<button aria-label="Close" onclick="close()">X</button>
```

## References

- [10 guidelines to improve your web accessibility](https://aerolab.co/blog/web-accessibility/)
- [Using the button role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_button_role)
