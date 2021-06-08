### Module Export & Import

Javascript  မှာအရင်က js file တွေကို တစ်နေရာကနေတနေရာသုံးချင်ရင် HTML ထဲမှာ script အဖွင့်အပိတ် tag ထဲမှာပဲ ရေးရလေ့ရှိတယ်ဗျ။ အခု ES6 ရောက်လာတဲ့အချိန်မှာသာ module export လုပ်ပီးရေးလို့ရလာတာ။ Example ကြည့်လိုက်ရအောင်

`Example - 1 `

```javascript
greeting.js

const greeting = () => {
	console.log("Hello");
}

export default greeting;
```

```javascript
utility.js

export const getName = () => {
    console.log("My superhero name is Batman")
}

export const getCity = () => {
	console.log("City name is Gotham City ")
}
```

```
app.js

import greeting from "./greeting.js"
import greet from "./greeting,js"

import {getName} from "./utility.js"
import {getCity} from "./utility.js"
```

အပေါ်မှာပြထားတဲ့ example မှာဆိုရင် greeting.js မှာ default keyword ကိုသုံးထားတာတွေရလိမ့်မယ်။ default က ဘာလိုပြောချင်တာလဲဆိုတော့ greeting.js ကို ခေါ်သုံးသမျှ သူက default အနေနဲ့ example အရဆို greeting ဆိုတဲ့ Function ကိုပဲ သူကညွှန်ပေးလိမ့်ဗျ။  app.js မှာ greeting.js  ကိုနှစ်ခါခေါ်ထားတာတွေ့ရတယ်  import နောက်က ပေးတဲ့ name  ကိုတော့ကြိုက်တာပေးလို့ရတယ် ဒါပေမဲ့စောနကပြောသလိုသူက သူ default အနေနဲ့ပေးထားတာပဲ ညွှန်ပေးမှာပဲ။ utility.js  မှာဆိုရင် default keyword ပေးမထားတဲ့အတွက် သူကိုခေါ်သုံးချင်ရင်တိကျတဲ့ name ပေးခေါ်မှရတော့တယ် အဲ့တာကို ဘယ်လိုခေါ်သုံးရလဲဆိုတာ app.js  မှာရေးပြထားတာကိုကြည့်လိုက်ရင်နားလည်မယ်ထင်ပါတယ်။ အဲ့တာကို ကိုယ်ကြိုက်တဲ့ name  ပေးပီးရေးချင်ရင်လဲရပါသေးတယ်ဗျာ....

`Example - 2`

```javascript
app.js

import greeting from "./greeting.js"
import greet from "./greeting,js"

import {getName} from "./utility.js"
import {getCity} from "./utility.js"

// eg - 1 
import {getName as  name} from "./utility.js"

// eg - 2
import * as superhero from "./utility.js"
```

Example - 2  မှာဆိုရင်အသစ်နှစ်ခုပါလာတယ်  eg - 1မှာအပေါ်ကပြောခဲ့သလို custom name ပေးပီးသုံးချင်ရင် ရေးရတဲပုံစံဖစ်ပီး  eg - 2 ကတော့ * ကိုသုံးပီးရှိသမျှ utility.js ထဲက အရာတွေကို superhero ဆိုပီးနာမည်တပ်သုံးလိုက်တယ်။ ပြောချင်တာက * ဆိုတာက ရှိသမျှအားလုံးကိုဆိုလိုတယ်ဆိုတာသိထားရင်ရပီ။ 

