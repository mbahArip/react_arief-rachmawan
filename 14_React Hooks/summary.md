# 14 React Hooks

## Resume

Pada materi ini saya mempelajari:

-   React Hooks
-   Implementasi useState dan useEffect
-   Custom Hooks

### React Hooks

#### Apa itu React Hooks?

React Hooks merupakan fitur baru di React 16.8. Dengan Hooks, kita dapat menggunakan state, dan fitur React yang lain tanpa perlu menulis sebuah kelas.

Beberapa contoh hooks pada react:

-   useState
-   useEffect
-   useContext
-   useReducer
-   useCallback
-   useMemo
-   useRef
-   useImperativeHandle
-   useLayoutEffect
-   useDebugValue

#### Aturan pada hooks

Ada beberapa aturan yang harus dipenuhi oleh hooks:

-   Hanya panggil hooks di tingkat atas
    Jangan memanggil hooks di dalam loops, condition, atau nested function.
-   Hanya panggil hooks dari fungsi React
    Jangan memanggil hooks dari fungsi javascript biasa.

### Implementasi useState dan useEffect

#### Implementasi useState

Di dalam sebuah function component, kita tidak memiliki this. Sebagai gantinya kita gunakan hook useState secara langsung di dalam komponen kita.  
Contoh:

```jsx
import { useState } from 'react';

function Example() {
	const [count, setCount] = useState(0);
	return <div>{count}</div>;
}
```

Berdasarkan contoh diatas, count merupakan variable untuk mengambil value state, dan setCount merupakan variable untuk mengubah value state, dan nilai 0 di dalam argumen useState merupakan default value dari state tersebut.

#### Implementasi useEffect()

useEffect adalah sebuah function yang digunakan untuk mengimplementasikan fungsi React yang bersifat asynchronous.  
Ada dua jenis useEffect, yaitu yang butuh pembersihan dan tidak butuh pembersihan.

#### Contoh tanpa pembersihan:

```jsx
import { useState, useEffect } from 'react';

function Example() {
	const [count, setCount] = useState(0);
	useEffect(() => {
		document.title = `You clicked ${count} times`;
	}, [count]);
	return (
		<div>
			<p>You clicked {count} times</p>
			<button onClick={() => setCount(count + 1)}>Click me</button>
		</div>
	);
}
```

Pada code diatas, kita tidak perlu melakukan pembersihan dikarenakan useEffect akan mereturn untuk mengganti title pada document, setiap variable count berubah.

#### Contoh dengan pembersihan:

```jsx
import { useState, useEffect } from 'react';

function Example() {
	const [count, setCount] = useState(0);

	useEffect(() => {
		let interval = setInterval(() => {
			console.log(`Count now is: ${count}`);
		}, 1000);

		return clearInterval(interval);
	}, [count]);
}
```

Untuk code diatas, kita perlu untuk membersihkan interval, apabila kita tidak menggunakan clearInterval, maka interval akan terus berjalan dan akan membuat interval baru setiap kali state count berubah.

### Custom Hooks

#### Apa itu Custom Hooks?

Custom Hooks berarti membuat hook kita sendiri, memungkinkan kita mengekstrak komponen logika ke fungsi yang dapat digunakan lagi.

#### Contoh Custom Hooks

Bayangkan kita mempunya code berikut di dalam sebuah component:

```jsx
import { useState, useEffect } from 'react';

const MyComponent = () => {
	const [onSmallScreen, setOnSmallScreen] = useState(false);

	useEffect(() => {
		checkScreenSize();
		window.addEventListener('resize', checkScreenSize);
	}, []);

	let checkScreenSize = () => {
		setOnSmallScreen(window.innerWidth < 768);
	};

	return (
		<div className={`${onSmallScreen ? 'small' : 'large'}`}>
			<h1> Hello World!</h1>
		</div>
	);
};
```

Kita ingin function checkScreenSize() dapat dijalankan dibanyak component, dan menulis function tersebut berulang kali akan membuang waktu kita.  
Maka kita bisa buat function tersebut menjadi Custom Hooks.

Kita dapat membuat file baru bernama useWindowWidth, dan simpan file tersebut di folder hooks.

```jsx
import { useState, useEffect } from 'react';

const useWindowWidth = () => {
	const [isScreenSmall, setIsScreenSmall] = useState(false);

	let checkScreenSize = () => {
		setIsScreenSmall(window.innerWidth < 600);
	};
	useEffect(() => {
		checkScreenSize();
		window.addEventListener('resize', checkScreenSize);

		return () => window.removeEventListener('resize', checkScreenSize);
	}, []);

	return isScreenSmall;
};

export default useWindowWidth;
```

Setelah kita buat file custom hooks seperti berikut, kita dapat mengubah code di dalam component yang kita buat menjadi:

```jsx
import useWindowWidth from './hooks/useWindowWidth';

const MyComponent = () => {
	const onSmallScreen = useWindowWidth();

	return (
		<div className={`${onSmallScreen ? 'small' : 'large'}`}>
			<h1> Hello World!</h1>
		</div>
	);
};
```

---

## Task

Untuk task kali ini, saya hanya harus mengubah code dari task sebelumnya, yang asalnya menggunakan class component, menjadi function component.

Source code dapat dilihat di [Github Repository](https://www.github.com/mbaharip/Assignment-Todo-List-2)
