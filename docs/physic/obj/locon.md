# Location Object Context (object)

```Diego
begin_locon();
    heed_map(21_toyne);
    add_object(teabag)_indef()
    with_locon()_object(teabag)_state(inprogress);
    with_locon()_at(8.5,2.6);
    with_locon()_look(teabag_001.jpg)_see(teabag_001.svg);
end_locon()

begin_locon();
    heed_map(21_toyne);
    add_object(teabag)_indef()
    with_locon()_object(teabag)_state(unused);
    with_locon()_at(8.5,2.6);
    with_locon()_look()_file(teabag_002.jpg);
    with_locon()_see()_file(teabag_002.svg);
end_locon()

begin_locon()
    heed_map(21_toyne);
    add_object(butter)_indef()_consumeable();
    add_textmark(bb_stamp)_text(BEST BEFORE\n31 JUL 21\n06:43 L 029)_see(bb_text);

    with_locon()_object(butter)_form(block);
    add_object


```
https://cocodataset.org/#explore



| `{type}` | operator | coco | description | API |
| --- | --- | --- | --- | --- |
| <a name="person"></a> `{person}` | 🧍 | ![coco](https://cocodataset.org/images/cocoicons/1.jpg) | person | [human](./human.md) |
| <a name="bicycle"></a> `{bicycle}` | 🚲 | ![coco](https://cocodataset.org/images/cocoicons/2.jpg) | bicycle | [vehicle](./vehicle.md#bicycle) |
| <a name="car"></a> `{car}` | 🚗 | ![coco](https://cocodataset.org/images/cocoicons/3.jpg) | car | [vehicle](./vehicle.md#car) |
| <a name="motorcycle"></a> `{motorcycle}` &nbsp; `{motorbike}` | 🏍 | ![coco](https://cocodataset.org/images/cocoicons/4.jpg) | motorcycle | [vehicle](./vehicle.md#motorcycle) |
| <a name="airplane"></a> `{airplane}` | ✈ &nbsp; 🛩 | ![coco](https://cocodataset.org/images/cocoicons/5.jpg) | airplane | [vehicle](./vehicle.md#airplane) |
| <a name="bus"></a> `{bus}` | 🚌 | ![coco](https://cocodataset.org/images/cocoicons/6.jpg) | bus | [vehicle](./vehicle.md#bus) |
| <a name="train"></a> `{train}` &nbsp; `{loco}` | 🚆 | ![coco](https://cocodataset.org/images/cocoicons/7.jpg) | train | [vehicle](./vehicle.md#train) |
| <a name="truck"></a> `{truck}` &nbsp; `{lorry}` | 🚚 | ![coco](https://cocodataset.org/images/cocoicons/8.jpg) | truck | [vehicle](./vehicle.md#truck) |
| <a name="boat"></a> `{boat}` &nbsp; `{lorry}` | ⛵ &nbsp; 🛥 | ![coco](https://cocodataset.org/images/cocoicons/9.jpg) | boat | [vehicle](./vehicle.md#boat) |
| <a name="traffic_light"></a> `{traffic_light}` &nbsp; `{traff}` | 🚦 | ![coco](https://cocodataset.org/images/cocoicons/10.jpg) | traffic lights | [mobot](./mobot.md#tl) |
| <a name="fire hydrant"></a> `{fire hydrant}` &nbsp; `{firehy}` | <span class="material-symbols-outlined">fire_hydrant</span> | ![coco](https://cocodataset.org/images/cocoicons/11.jpg) | fire hydrant | [object](./object.md#firehy) |
| <a name="road_sign"></a> `{road_sign}` | <span class="material-symbols-outlined">signpost</span> | ![coco](https://cocodataset.org/images/cocoicons/12.jpg) | road sign | [object](./object.md#road_sign) |
| <a name="stop_sign"></a> `{stop_sign}` | 🛑 | ![coco](https://cocodataset.org/images/cocoicons/13.jpg) | stop sign | [object](./object.md#stop_sign) |
| <a name="parking_meter"></a> `{parking_meter}` | 🅿️ | ![coco](https://cocodataset.org/images/cocoicons/14.jpg) | parking meter | [mobot](./mobot.md#parking_meter) |
| <a name="bench"></a> `{bench}` |  | ![coco](https://cocodataset.org/images/cocoicons/15.jpg) | bench | [object](./object.md#bench) |
| <a name="bird"></a> `{bird}` | 🐦 | ![coco](https://cocodataset.org/images/cocoicons/16.jpg) | bird | [organic](./organic.md#bird) |
| <a name="cat"></a> `{cat}` | 🐈 | ![coco](https://cocodataset.org/images/cocoicons/17.jpg) | cat | [organic](./organic.md#cat) |
| <a name="dog"></a> `{dog}` | 🐕 | ![coco](https://cocodataset.org/images/cocoicons/18.jpg) | dog | [organic](./organic.md#dog) |
| <a name="horse"></a> `{horse}` | 🐎 &nbsp; 🐴 | ![coco](https://cocodataset.org/images/cocoicons/19.jpg) | horse | [organic](./organic.md#horse) |
| <a name="sheep"></a> `{sheep}` | 🐑 | ![coco](https://cocodataset.org/images/cocoicons/20.jpg) | sheep | [organic](./organic.md#sheep) |
| <a name="cow"></a> `{cow}` | 🐄 &nbsp; 🐮 | ![coco](https://cocodataset.org/images/cocoicons/21.jpg) | cow | [organic](./organic.md#cow) |
| <a name="elephant"></a> `{elephant}` | 🐘 | ![coco](https://cocodataset.org/images/cocoicons/22.jpg) | elephant | [organic](./organic.md#elephant) |
| <a name="bear"></a> `{bear}` | 🐻 | ![coco](https://cocodataset.org/images/cocoicons/23.jpg) | bear | [organic](./organic.md#bear) |
| <a name="zebra"></a> `{zebra}` | 🦓 | ![coco](https://cocodataset.org/images/cocoicons/24.jpg) | zebra | [organic](./organic.md#zebra) |
| <a name="giraffe"></a> `{giraffe}` | 🦒 | ![coco](https://cocodataset.org/images/cocoicons/25.jpg) | giraffe | [organic](./organic.md#giraffe) |
| <a name="teacup"></a> `{teacup}` | 🍵 | ![coco](https://cocodataset.org/images/cocoicons/26.jpg) | teacup | [object](./object.md#teacup) |
| <a name="backpack"></a> `{backpack}` | 🎒 | ![coco](https://cocodataset.org/images/cocoicons/27.jpg) | backpack | [object](./object.md#backpak) |
| <a name="umbrella"></a> `{umbrella}` | ☂ | ![coco](https://cocodataset.org/images/cocoicons/28.jpg) | umbrella | [object](./object.md) |
| <a name="shoe"></a> `{shoe}` | 👞 | ![coco](https://cocodataset.org/images/cocoicons/29.jpg) | shoe | [object](./object.md#shoe) |
| <a name="spectacles"></a> `{specs}` &nbsp; `{glasses}` &nbsp; `{specs}` | 👓 | ![coco](https://cocodataset.org/images/cocoicons/30.jpg) | glasses | [object](./object.md#glasses) |
| <a name="handbag"></a> `{handbag}` &nbsp; `{clutch}` | 👜 | ![coco](https://cocodataset.org/images/cocoicons/31.jpg) | zebra | [object](./object.md#handbag) |
| <a name="tie"></a> `{tie}` | 👔 | ![coco](https://cocodataset.org/images/cocoicons/32.jpg) | tie | [object](./object.md#tie) |
| <a name="luggage"></a> `{luggage}` &nbsp; `{suitcase}` | 🧳 | ![coco](https://cocodataset.org/images/cocoicons/33.jpg) | luggage | [object](./object.md#luggage) |
| <a name="frisbee"></a> `{frisbee}` | 🥏 | ![coco](https://cocodataset.org/images/cocoicons/34.jpg) | frisbee | [object](./object.md#frisbee) |
| <a name="skis"></a> `{skis}` | 🎿 | ![coco](https://cocodataset.org/images/cocoicons/35.jpg) | skis | [object](./object.md#skis) |
| <a name="snowboard"></a> `{snowboard}` | 🏂 | ![coco](https://cocodataset.org/images/cocoicons/36.jpg) | snowboard | [object](./object.md#snowboard) |
| <a name="ball"></a> `{sports_ball}` &nbsp; `{ball}` | ⚽ | ![coco](https://cocodataset.org/images/cocoicons/37.jpg) | ball | [object](./object.md#ball) |
| <a name="kite"></a> `{kite}` | 🪁 | ![coco](https://cocodataset.org/images/cocoicons/38.jpg) | kite | [object](./object.md#kite) |
| <a name="bat"></a> `{sports_bat}` | 🏏 | ![coco](https://cocodataset.org/images/cocoicons/39.jpg) | sports bat | [object](./object.md#sports_bat) |
| <a name="sports_glove"></a> `{sports_glove}` | 👔 | ![coco](https://cocodataset.org/images/cocoicons/40.jpg) | sports glove | [object](./object.md#sports_glove) |
| <a name="skateboard"></a> `{skateboard}` | 🛹 | ![coco](https://cocodataset.org/images/cocoicons/41.jpg) | skateboard | [object](./object.md#skateboard) |
| <a name="surfboard"></a> `{surfboard}` | 🏄 | ![coco](https://cocodataset.org/images/cocoicons/42.jpg) | surfboard | [object](./object.md#surfboard) |
| <a name="sports_racket"></a> `{sports_racket}` &nbsp; `{tennis_racket}` | 🎾 | ![coco](https://cocodataset.org/images/cocoicons/43.jpg) | tennis racket | [object](./object.md#sports_racket) |
| <a name="bottle"></a> `{bottle}` | 🧴 | ![coco](https://cocodataset.org/images/cocoicons/44.jpg) | bottle | [object](./object.md#bottle) |
| <a name="plate"></a> `{plate}` | 🍽️ | ![coco](https://cocodataset.org/images/cocoicons/45.jpg) | plate | [object](./object.md#plate) |
| <a name="wine_glass"></a> `{wine_glass}` | 🍷 | ![coco](https://cocodataset.org/images/cocoicons/46.jpg) | wine glass | [object](./object.md#wine_glass) |
| <a name="cup"></a> `{cup}` &nbsp; `{glass}` | 🥤 &nbsp; 🥛 &nbsp; 🥃 | ![coco](https://cocodataset.org/images/cocoicons/47.jpg) | cup | [object](./object.md#cup) |
| <a name="fork"></a> `{fork}` | 🍴 | ![coco](https://cocodataset.org/images/cocoicons/48.jpg) | fork | [object](./object.md#fork) |
| <a name="knife"></a> `{knife}` | 🍴 | ![coco](https://cocodataset.org/images/cocoicons/49.jpg) | knife | [object](./object.md#knife) |
| <a name="spoon"></a> `{spoon}` | 🥄 | ![coco](https://cocodataset.org/images/cocoicons/50.jpg) | spoon | [object](./object.md#spoon) |
| <a name="bowl"></a> `{bowl}` | 🥣 | ![coco](https://cocodataset.org/images/cocoicons/51.jpg) | bowl | [object](./object.md#bowl) |
| <a name="banana"></a> `{banana}` | 🍌 | ![coco](https://cocodataset.org/images/cocoicons/52.jpg) | banana | [organic](./organic.md#banana) |
| <a name="apple"></a> `{apple}` | 🍏 &nbsp; 🍎 | ![coco](https://cocodataset.org/images/cocoicons/53.jpg) | apple | [organic](./organic.md#apple) |
| <a name="sandwich"></a> `{sandwich}` | 🥪 | ![coco](https://cocodataset.org/images/cocoicons/54.jpg) | sandwich | [organic](./organic.md#sandwich) |
| <a name="orange"></a> `{orange}` | | ![coco](https://cocodataset.org/images/cocoicons/55.jpg) | orange | [organic](./organic.md#orange) |
| <a name="broccoli"></a> `{broccoli}` | 🥦 | ![coco](https://cocodataset.org/images/cocoicons/56.jpg) | broccoli | [organic](./organic.md#broccoli) |
| <a name="carrot"></a> `{carrot}` | 🥕 | ![coco](https://cocodataset.org/images/cocoicons/57.jpg) | carrot | [organic](./organic.md#carrot) |
| <a name="hot_dog"></a> `{hot_dog}` | 🌭 | ![coco](https://cocodataset.org/images/cocoicons/58.jpg) | hot dog | [object](./organic.md#hot_dog) |
| <a name="pizza"></a> `{pizza}` | 🍕 | ![coco](https://cocodataset.org/images/cocoicons/59.jpg) | pizza | [object](./organic.md#pizza) |
| <a name="doughnut"></a> `{doughnut}` &nbsp; `{donut}` | 🍩 | ![coco](https://cocodataset.org/images/cocoicons/60.jpg) | doughnut | [object](./object.md#doughnut) |
| <a name="cake"></a> `{cake}` | 🎂 | ![coco](https://cocodataset.org/images/cocoicons/61.jpg) | cake | [object](./object.md#cake) |
| <a name="chair"></a> `{chair}` | 🪑 | ![coco](https://cocodataset.org/images/cocoicons/62.jpg) | chair | [object](./object.md#chair) |
| <a name="couch"></a> `{couch}` &nbsp; `{sofa}` &nbsp; `{settee}` | 🛋️ | ![coco](https://cocodataset.org/images/cocoicons/63.jpg) | couch | [object](./object.md#couch) |
| <a name="potted_plant"></a> `{potted_plant}` | 🪴 | ![coco](https://cocodataset.org/images/cocoicons/64.jpg) | potted plant | [object](./object.md#potted_plant) |
| <a name="bed"></a> `{bed}` | 🛏️ | ![coco](https://cocodataset.org/images/cocoicons/65.jpg) | bed | [object](./object.md#bed) |
| <a name="picture"></a> `{picture}` | 🖼️ | ![coco](https://cocodataset.org/images/cocoicons/66.jpg) | picture | [object](./object.md#) |
| <a name="dining_table"></a> `{dining_table}` &nbsp; `{table}` | <span class="material-symbols-outlined">table_restaurant</span> | ![coco](https://cocodataset.org/images/cocoicons/67.jpg) | dining table | [object](./object.md#dining_table) |
| <a name="window"></a> `{window}` | 🪟 | ![coco](https://cocodataset.org/images/cocoicons/68.jpg) | window | [object](./object.md#) |
| <a name="desk"></a> `{desk}` | <span class="material-symbols-outlined">desk</span> | ![coco](https://cocodataset.org/images/cocoicons/69.jpg) | desk | [object](./object.md#desk) |
| <a name="wc"></a> `{wc}` &nbsp; `{toilet}` &nbsp; `{toilet_seat}` | 🚽 | ![coco](https://cocodataset.org/images/cocoicons/70.jpg) | toilet  | [object](./object.md#wc) |
| <a name="door"></a> `{door}` | 🚪 | ![coco](https://cocodataset.org/images/cocoicons/71.jpg) | door | [object](./object.md#door) |
| <a name="tv"></a> `{tv}` &nbsp; `{television}` | 📺 | ![coco](https://cocodataset.org/images/cocoicons/72.jpg) | laptop | [computer](./object.md#computer) |
| <a name="laptop"></a> `{laptop}` | 💻 | ![coco](https://cocodataset.org/images/cocoicons/73.jpg) | laptop | [computer](./object.md#computer) |
| <a name="mouse"></a> `{mouse}` | 🖱️ | ![coco](https://cocodataset.org/images/cocoicons/74.jpg) | mouse | [object](./object.md#computer_mouse) |
| <a name="remote"></a> `{remote}` | <span class="material-symbols-outlined">remote_gen</span> | ![coco](https://cocodataset.org/images/cocoicons/75.jpg) | remote | [object](./object.md#remote) |
| <a name="keyboard"></a> `{keyboard}` | ⌨️ | ![coco](https://cocodataset.org/images/cocoicons/76.jpg) | keyboard | [mobot](./mobot.md#keyboard) |
| <a name="cellphone"></a> `{cellphone}` &nbsp; `{mobile_phone}` &nbsp; `{mobile}` | 📱 | ![coco](https://cocodataset.org/images/cocoicons/77.jpg) | cellphone | [mobot](./mobot.md#cellphone) |
| <a name="microwave"></a> `{microwave}` &nbsp; `{microwave_oven}` | <span class="material-symbols-outlined">microwave</span> | ![coco](https://cocodataset.org/images/cocoicons/78.jpg) | microwave | [applian](./applian.md#microwave) |
| <a name="oven"></a> `{oven}` | <span class="material-symbols-outlined">oven_gen</span> | ![coco](https://cocodataset.org/images/cocoicons/79.jpg) | oven | [applian](./applian.md#oven) |
| <a name="toaster"></a> `{toaster}` |  | ![coco](https://cocodataset.org/images/cocoicons/80.jpg) | toaster | [applian](./applian.md#toaster) |
| <a name="sink"></a> `{sink}` &nbsp;  | <span class="material-symbols-outlined">countertops</span> | ![coco](https://cocodataset.org/images/cocoicons/81.jpg) | sink | [object](./object.md#sink) |
| <a name="fridge"></a> `{fridge}` &nbsp; `{refrigerator}` &nbsp; `{freezer}` &nbsp; `{fridge_freezer}` |  | ![coco](https://cocodataset.org/images/cocoicons/82.jpg) |  | [object](./object.md#) |
| <a name="blender"></a> `{blender}` | :fa-blender: | ![coco](https://cocodataset.org/images/cocoicons/83.jpg) | blender | [object](./object.md#blender) |
| <a name="book"></a> `{book}` | 📕 | ![coco](https://cocodataset.org/images/cocoicons/84.jpg) | book | [object](./object.md#book) |
| <a name="clock"></a> `{clock}` | ⏰ &nbsp; ⏲️ | ![coco](https://cocodataset.org/images/cocoicons/85.jpg) | clock | [sobot](./sobot.md#clock) |
| <a name="vase"></a> `{vase}` | 🏺 | ![coco](https://cocodataset.org/images/cocoicons/86.jpg) | vase | [object](./object.md#vase) |
| <a name="scissors"></a> `{scissors}` | ✂️ | ![coco](https://cocodataset.org/images/cocoicons/87.jpg) | scissors | [object](./object.md#scissors) |
| <a name="teddy_bear"></a> `{teddy_bear}` &nbsp; `{plush_toy}` | 🧸 | ![coco](https://cocodataset.org/images/cocoicons/88.jpg) | teddy bear | [object](./object.md#teddy_bear) |
| <a name="hairdrier"></a> `{hairdrier}` &nbsp; `{hair_drier}` |  | ![coco](https://cocodataset.org/images/cocoicons/89.jpg) | hairdrier | [object](./object.md#hairdrier) |
| <a name="toothbrush"></a> `{toothbrush}` | 🪥 | ![coco](https://cocodataset.org/images/cocoicons/90.jpg) | toothbrush | [object](./object.md#toothbrush) |
| <a name="hairbrush"></a> `{hairbrush}` | | ![coco](https://cocodataset.org/images/cocoicons/91.jpg) | hairbrush | [object](./object.md#hairbrush) |





https://cocodataset.org/#home

