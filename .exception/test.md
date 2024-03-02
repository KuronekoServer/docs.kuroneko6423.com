---
title: テスト用ページ
---

<script>
switch(document.readyState){
  case 'complete':
    new multi_language()
    break
  default:
    window.addEventListener('load' , (()=>{
      new multi_language()
    }))
}

function multi_language(){
  this.set_current_lang()
}
multi_language.prototype.get_lang_lists = function(){
  return document.querySelectorAll(`input[type='radio'][name='lang']`)
}
multi_language.prototype.set_current_lang = function(){
  const current_lang = document.querySelector('html').getAttribute('lang')
  this.checked_lang_list(current_lang)
}
multi_language.prototype.checked_lang_list = function(current_lang){
  const elms = this.get_lang_lists()
  for(const elm of elms){
    if(elm.value === current_lang){
      elm.checked = true
    }
    elm.addEventListener('click' , this.click_lang.bind(this))
  }
}
multi_language.prototype.click_lang = function(e){
  const lang = e.target.value
  document.querySelector('html').setAttribute('lang' , lang)
}
</script>

<style>
.language-change{
  display:flex;
  gap:10px;
  margin:10px;
  align-items:center;
  cursor:pointer;
}

html[lang='ja'] *:is([lang]):not([lang='ja']),
html[lang='en'] *:is([lang]):not([lang='en']),
html[lang='de'] *:is([lang]):not([lang='de']){
  display:none!important;
}
</style>

<div class='language-change'>
   <label><input type='radio' name='lang' value='ja' checked>日本語</label>
   <label><input type='radio' name='lang' value='en'>English</label>
   <label><input type='radio' name='lang' value='de'>Deutsch</label>
</div>

:::{lang="ja"}
こんにちは
:::

:::{lang="en"}
Hi
:::

:::{lang="de"}
Hi
:::