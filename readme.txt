npm init -y

npm i pug

npm install pug-cli -g

pug src/index.pug

pug src/index.pug -P

pug ./src -P -w

-------------------

npm i sass

npm install -g sass

--------------------


npm install -g npm-run-all

npm install -g live-server

------------

npm init stylelint


--------------------

  prefix pre-
  suffix -suf


----------------

  ---BEM---

Block Element Modification

В блоки нельзя позиционировать! А елементы можно.

# 1 - mix
всю позицию с ".block" переносим в ".header__block"

.header                     // position: relative;
  .block.header__block      // position: absolute
    .block__element         // position: absolute ❌

❗️ Но из-за єтого может возникнуть проблема когда в 
  ".block" необходимо позицонировать внутрение елементы
  ".block__element" как absolute.


# 2 - чтоб решить єту проблему
.header                     // position: relative; ✅
  .block.header__block      // position: absolute; ✅
    .block__content         // position: relative; ✅
      .block__element       // position: absolute; ✅

✅ Для .block__content ставми "position: relative;"
  тогда абсолуютные елементы не слетят.

или просто обертка

# 3 - wrapper
.header                 // position: relative; ✅
  .header__block        // position: absolute; ✅
    .block              // position: relative; ✅
      .block__element   // position: absolute; ✅

