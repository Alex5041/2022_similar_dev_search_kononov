# 2022_similar_dev_search_kononov

### Описание проекта
Этот проект нужен, чтобы искать похожих разработчиков. **Схожесть** — это метрика, которая может вычисляться на основе разных данных, например:
* Языки программирования, на которых пишут разработчики;
* Комментарии к коду;
* Схожесть написанного кода.

### Этапы проекта
Ориентировочно проект будет состоять из 7 этапов^
1) **Discover**: Найти репозитории на гитхабе;
2) **Clone**: Скопировать репозитории к себе;
3) **Handle VCS**: Разобраться с системой контроля версий, чтобы сделать следующие шаги;
4) **Classify**: Сгруппировать собранные репозитории. Возможно, вариантов группировок будет несколько (примеры: по ЯП, по разработчику, по дате...). Сделать с помощью enry[^1].
5) **Filter**: Оставить только те репозитории, с которыми **удобно**[^2] работать
6) **Parse**: Извлечь из оставшихся репозиториев те данные, на основе которых будет вычисляться схожесть. Разумно представить код в виде AST-дерева, используя tree-sitter[^3]
7) **Analyze**: Проанализировать схожесть, сделать вывод.

### Оценивание проекта
Оценка за проект складывается из выполненных этапов: Grade = github_api * **0.15** + git * **0.25** + enry[^1] * **0.2** + tree_sitter[^3] * **0.25** + similar_dev_search * **0.15**
 
 [^1]: классификатор языков программирования https://github.com/go-enry/go-enry
 [^2]: пока не ясно, что значит удобно

 [^3]: библиотека для извлечения AST из кода https://github.com/tree-sitter/tree-sitter