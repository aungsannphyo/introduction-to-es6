### Variables

#### 1. Var

ပုံမှန်အားဖြင့် Vanilla Javascript မှာ variables ကြော်ငြာတဲ့အခါ var ဆိုတဲ့ keyword ကိုအသုံးပြုကြတယ်။

Example - 1

> ​		var counter = 5;
>
> ​		console.log(counter);	Answer => 5
>
> ​		var counter =  10;
>
> ​		console.log(counter);	Answer => 10



Example - 2

> ​		var counter = 5;
>
> ​		console.log(counter);	Answer => 5
>
> ​		counter =  10;
>
> ​		console.log(counter);	Answer => 10



အပေါ်က example ၁ နဲ့  ၂ မှာ var အသုံးပြုပုံကို ပြောပြထားတာဖစ်တယ်။ example ၁  မှာဆိုရင် counter ဆိုပီး variable ကြော်ငြာပီး  5 ကို assign လုပ်လိုက်တယ် ပီးတော့ နောက်အဲ့နာမည်တိုင်းပဲ ကြော်ငြာပီး 10 ကို assign  ထပ်လုပ်တယ် အဲ့တော့ပထမတစ်ခုကို overwrite ဖစ်သွားပီး နောက်ဆုံးမှာ အဖြေက 10 ဖစ်သွားတယ် ။  variable name တူတူ နှစ်ခါ declare  လုပ်တာကို error တက်မသွားပဲ အဖြေရတော့  ကိုယ့် Project  မှာ var keyword  ကိုသုံးပီး ရေးတဲ့အခါတိုင်ပတ်တဲ့အချိန်တွေရှိနိုင်ပီး နည်းနည်း messy ဖစ်တယ်။ example 2 မှာလဲ လုပ်ငန်းပုံစံက တူတူပေမဲ့ declare လုပ်ထားတဲ့  counter ထဲ ကိုပဲ overwrite ထပ်လုပ်ပီး နောက်ဆုံး အဖြေက  10 ဖစ်သွားတယ်။

var ကို scoped variable or globally variable အနေနဲ့သုံးလို့ရတယ်။

Example - 3

> var counter = 5;
>
> function sayName() {
>
> ​	console.log(counter);
>
> ​	var superHeroName = "Batman";
>
> ​	console.log(superHeroName);
>
> }
>
> sayName();	
>
> Answer =>	5
>
> ​					 Batman
>
> console.log(name)
>
> ReferenceError: name is not defined

Example 3 မှာဆိုရင် counter က global variable ဖစ်ပီး name  က scope variable ဖစ်တယ်။ scope variable ဆိုတာသူသတ်မှတ်ထားတဲ့အပိုင်းထဲမှာပဲသုံးခွင့်ရှိတာကိုပြောချင်တာဖစ်တယ် အာ့ကြောင့်  console.log(name)  ဆိုပီး  { }  အပြင်ကနေ name ကိုအဖြေထုတ်ကြည့်တဲ့အခါ error တက်သွားတာကိုတွေ့ရလိမ့်မယ်။ 



#### 2 . Let  

let and const keyword တွေက ES6 မှ စတင်ပါ၀င် လာတာဖစ်ပီး  ES6 ဆိုတာက ၂၀၁၅ မှာ ဖန်တီးခဲ့တဲ့ အတွက် ECMAScript 2015 or ECMAScript 6 လို့ခေါ်ကြတယ်။ သူကဘာတွေလုပ်ဆောင်ပေးသလဲဆိုရင် လက်ရှိ Javascript (ES5) မှာအသုံး၀င်တဲ့ လုပ်ဆောင်ချက်ပေါင်းများစွာကို အဆင့်မြှင့်ပီး ပို၍လွယ်ကူအောင်  easier for devs to code လို့ရအောင်လုပ်ဆောင်ပေးထားတာဖစ်တယ်။ React ကျရင်လဲ  ES6   ကိုပဲ အဓိက ထားသုံးမှာမို့ မဖစ်မနေသိထားရမဲ့ အရာတစ်ခုဖစ်တဲ့အတွက် သေချာကြည့်ထားဖို့လိုမယ်ဗျ။ ကဲ အာ့ဆို  let keyword usage ကြည့်လိုက်ရအောင် ...



Example - 4 

> let superHeroName = "Batman"
>
> console.log(superHeroName);	Answer  => Batman

သူ့ကိုအသုံးပြုပုံကလဲ var နဲ့တူတူပဲ။ ကဲ အာဆို variable name တူတူပေးပီး သုံးကြည့်ရအောင်

Example - 5

> 