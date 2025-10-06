Всё, что помещается между открывающим и закрывающим тегами компонента [[React. Компонент]], передается в компонент как props.children.

Рассмотрим пример:
```js
const FancyParagraph = (props) => {
	<p style={{color: 'blue'}}>
		{props.children}
	</p>
};

const Card = (props) => {
	<>
		<FancyParagraph>Это раскрашенный параграф!</FancyParagraph>
	</>
};
```

children можно также передать явно в пропсы компонента:
```js
<FancyParagraph children={'Текст'} />
```

```js
<FancyParagraph children={'Текст'}>Приоритетный текст!</FancyParagraph>
```
Но в данном случае "Приоритетный текст" будет приоритетным дочерним контентом и именно он попадёт в props.children.
##### Источники
1. \[Яндекс.Практикум] React-разработчик (2024)

###### Доп. связи

###### Теги
