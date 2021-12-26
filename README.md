# exoplanets_visualization 

## folders: 
```
├───res
│   ├─── visualization 1 anim.gif
│   ├─── visualization 2 full.png
│   ├─── visualization 2 single category.png
│   └─── visualization 3 full.png
├───dataset
│   ├─── exoplanet.eu_catalog.csv        | main dataset with exoplanets data. 
|   |                                    |        Sourse: http://exoplanet.eu/
│   ├─── planets_raw.csv                 | additional dataset with Solar System plnets data. 
|   |                                    |        Sourse: https://github.com/devstronomy/nasa-data-scraper
│   ├─── planets.csv                     | processed planets dataset with values in Jupiters units
│   ├─── transform_planets_dataset.ipynb | file to process raw planets dataset
│   └─── exoplanet.eu_catalog.hyper      | data sourse for tableau
├───visualization 1
│   ├─── visualization1.ipynb            | jupyter notebook of visualization with slider
│   ├─── visualization1_animation.py     | visualization as git animated file
│   └─── visualization1.py               | visualization with slider
└───visualization 2-3
    └─── exoplanets.twb                  | tableau project with visualization
```
## comments:
In this project I am visualizing the dataset of discovered exoplenets.  
An [exoplanet](https://en.wikipedia.org/wiki/Exoplanet) or extrasolar planet is a planet outside the Solar System.  


### Visualization 1 Orbits and temperatures of known exoplanets

Ця візуалізація зроблена за допомогою бібліотеки matplotlib. Це обумовлено необхідністю відмальовувати велику кількість елепсів з конкретними параметрами.  
Для можливості взаємодіяти з візуалізацією було добавлено слайдер для масштабу зображення. Графік matplotlib не можна конвертуати в вебформат, тому для інтерактивної взаємодії потрібно запустити візуалізацію:
 - visualization 1/visualization1.ipynb
 - visualization 1/visualization1.py  

Для коректного відображення необхідно мати завантажений датасет.
 
Ці операції є досить незручними, тому для їх уникнення та можливості показати інтерактивність візуалізації я згенерував GIF анімацію, яка симулює інтеракцію з візуалізацією.  
![visualization 1 anim.gif](/res/visualization%201%20anim.gif?raw=true) 
На даній візуалізації можна побачити орбіти різних екзопланет.   
На візуалізації досит точно (не враховуючи похибки) передано форму та розміри орбіт, а також додано орбіти планет Сонячної системи для можливості порівняти їх зі знайомими величинами.  
Щоб уникнути викревлення сприйняття розмірів вирішено використовувати лінійну шкалу координат і використання слайдеру з вибором масштабу. Сам слайдер є логарифмічним, що дозволяє зручно його використовувати як на малих, так і на великих масштабах.  
Кут повороту орбіти було вибрано випадковим чином у проміжку між 0 і 90 градусів для диференціації еліптичних орбіт та природнього сприйняття.

### Visualization 2 History of exoplanets discovery

**Посилання на інтерактивну візуалізацію: [History of exoplanets discovery](https://public.tableau.com/views/exoplanetsdiscovery/Historyofexoplanetdiscovery?:language=en-US&:display_count=n&:origin=viz_share_link)**

![visualization 2 full.png](/res/visualization%202%20full.png?raw=true) 
<!-- On this visualization we can see the timeline of the exoplanet detection with distribution by the methods and distance to the planetary system. -->
На цій візуалізації ми можемо бачити розподіл відомих екзопланет за часом їх відкриття, відстанню до материнської зорі та способом знаходження.   
Візуалізація дозволяє зрозуміти історію дослідження екзопланет: побачити перші майже випадкові знахідки, згодом розвиток методу дослідження **радіальних швидкостей**, потім і метод **транзиту планети по диску зорі**, також і інші методи, які дозволяють "побачити" віддалені планети (**Мікролінзування**) або навпаки метод **прямого спостереження**, що дозволяє побачити близьк до нас світи.  
  
При виділенні певного методу можна закцентувати увагу тільки на екзопланетах знайдених цим методом:   
![visualization 2 single category.png](/res/visualization%202%20single%20category.png?raw=true) 


### Visualization 3 Size and mass of known exoplanets

**Посилання на інтерактивну візуалізацію: [Size and mass of known exoplanets](https://public.tableau.com/views/exoplanetssizeandmass/Sizeandmassofknownexoplanets?:language=en-US&:display_count=n&:origin=viz_share_link)**

![visualization 3 full.png](/res/visualization%203%20full.png?raw=true) 
На останній візуалізації можна побачити розподіл відомих екзопланет за їх розміром і масою.  
Усі дані подаються у одиницях маси чи радіусу Юпітера на логарифмічній шкалі.  
Для отримання точок від яких можна відштовхуватися до візуалізації додані планети Сонячної системи.  
З графіків чітко можна виділити кілька груп планет:  
- великі газові гіганти як Юпітер і Сатурн
- менші водно-газові планети типу Урана та Нептуна
- силікатні планети, яких нам відомо досить мало і вони не формують чітку групу, а швидше розрізнений хвіст
Така класифікація дозволяє зрозуміти, що зараз ми можемо побачити переважно великі та масивні екзопланети, які переважно є зовсім нецікавими для пошуку на них подібного на земне життя.


