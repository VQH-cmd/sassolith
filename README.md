![Sassolith](logo.svg)

# **Sassolith**

- 📦 *Toolkit:* **`Sassolith`**
- 🏗️ *Version:* **`2.0.0`**
- 👨‍💻 *Author:* [**VQH-cmd**](https://VQH-cmd.github.io)

<br/>

________________________________________________________________

<br/>

## **`[01]:` Description**

- CSS utility using **SASS & SCSS**.
- Customize CSS classes with your own style.

<br/>

________________________________________________________________

<br/>

## **`[02]:` Quick Start**

- This package is only implanted in [**Convergence ζ**](https://github.com/VQH-cmd/convergence.zeta) for now !

<br/>

________________________________________________________________

<br/>

## **`[03]:` Import**

<br/>

```scss
// style.sass
@import "<LOCATION_NAME>/_theme"
@import "<LOCATION_NAME>/_misc"
@import "<LOCATION_NAME>/_breakpoint"

@import "@vqh-cmd/sassolith"
```
```scss
// style.scss
@import "<LOCATION_NAME>/_theme";
@import "<LOCATION_NAME>/_misc";
@import "<LOCATION_NAME>/_breakpoint";

@import "@vqh-cmd/sassolith";
```

### **`🗃️` Global Files:**
- [**`<LOCATION_NAME>/_theme`**](example/variables/_theme.scss)
- [**`<LOCATION_NAME>/_misc`**](example/variables/_misc.scss)
- [**`<LOCATION_NAME>/_breakpoint`**](example/variables/_breakpoint.scss)

<br/>

> If using [**`node-sass-json-importer`**](https://www.npmjs.com/package/node-sass-json-importer)

```scss
// style.sass
@import "<LOCATION_NAME>/theme.json"
@import "<LOCATION_NAME>/misc.json"
@import "<LOCATION_NAME>/breakpoint.json"

@import "@vqh-cmd/sassolith"
```

```scss
// style.scss
@import "<LOCATION_NAME>/theme.json";
@import "<LOCATION_NAME>/misc.json";
@import "<LOCATION_NAME>/breakpoint.json";

@import "@vqh-cmd/sassolith";
```

### **`🗃️` Global Files:**
- [**`<LOCATION_NAME>/theme.json`**](example/variables/theme.json)
- [**`<LOCATION_NAME>/misc.json`**](example/variables/misc.json)
- [**`<LOCATION_NAME>/breakpoint.json`**](example/variables/breakpoint.json)

<br/>

________________________________________________________________

<br/>

## **`[04]:` Global Files**

<br/>

### **`theme`**
- [scss](example/variables/_theme.scss) | [json](example/variables/theme.json)

<br/>

### **`misc`**
- [scss](example/variables/_misc.scss) | [json](example/variables/misc.json)

<br/>

### **`breakpoint`**
- [scss](example/variables/_breakpoint.scss) | [json](example/variables/breakpoint.json)

<br/>

________________________________________________________________

<br/>

## **`[05]:` Config**

<br/>

### **`Basic`**
```scss
@include Sassolith((
	"class": (
		box-border,
		box-content,
	),
	"style": box-sizing,
	"value": (
		border-box,
		content-box,
	),
	"data": (
		"active": true,
		"important": false,
		"responsive": true,
		"state": (
			":required",
			":active",
			":hover",
			":visited",
		),
	),
));
```

<br/>
<br/>

### **`Color`**
```scss
@include Sassolith((
	"class": co,
	"style": color,
	"value": false,
	"data": (
		"active": true,
		"important": false,
		"responsive": true,
		"isColor": true,
		"state": (
			":hover",
		),
	),
));
```

<br/>
<br/>

### **`Formula`**
```scss
@include Sassolith((
	"class": w,
	"style": width,
	"value": false,
	"data": (
		"active": true,
		"important": false,
		"responsive": true,
		"formula": (
			"unit": (
				"class": "vw",
				"value": "vw",
			),
			"ratio": calc(1/10),
			"min": 0,
			"max": 1000,
			"step": 50,
		),
		"state": (
			":hover",
		),
	),
));
```

<br/>
<br/>

### **`Font Face`**
```scss
@include SassolithFont((
	"family": "Roboto",
	"name": "font1",
	"weight": (100, 200, 300, 400, 500, 600, 700, 800, 900),
	"style": (normal, italic),
	"src": "../fonts/",
	"format": (ttf, otf),
));
```
<br/>
<br/>

### [**Examples**](example/utilities/)

<br/>

________________________________________________________________

<br/>

## **`[06]:` Utility Function & Mixin**

<br/>

> Get **`$name`** from [**`theme`**](example/variables/theme.json).
- `theme » default » category » color`
- `theme » default » category » gradient`

<br/>

### **`co($name)`**
```scss
// 📟 scss
.co-m1 {color: co(m1);}

// 👉 output
.co-m1 {color: #0EF7D0;}
```

<br/>

### **`coTint($name, $percent)`**
```scss
// 📟 scss
.co-m1-t80 {color: coTint(m1, 80);}

// 👉 output
.co-m1-t80 {color: #cffdf6;}
```

<br/>

### **`coShade($name, $percent)`**
```scss
// 📟 scss
.co-m1-t80 {color: coShade(m1, 80);}

// 👉 output
.co-m1-t80 {color: #03312a;}
```

<br/>

### **`gra($name)`**
```scss
// 📟 scss
.grad-gra1 {background-color: gra(gra1);}

// 👉 output
.grad-gra1 {background-color: linear-gradient(90deg, #0EF7D0 0%, #6f9 100%);}
```

<br/>

> Get **`$media`** from [**`breakpoint`**](example/variables/breakpoint.json).

### **`res($media)`**
```scss
// 📟 scss
.fs-main {
	font-size: 24px;
	@include res(sm) {font-size: 20px;}
	@include res(xs) {font-size: 16px;}
}

// 👉 output
.fs-main {font-size: 24px;}
@media screen and (max-width: 800px) {
	.fs-main {font-size: 20px;}
}
@media screen and (max-width: 600px) {
	.fs-main {font-size: 18px;}
}
```

<br/>

________________________________________________________________

<br/>

Copyright © 2023, [VQH-cmd](https://VQH-cmd.github.io).