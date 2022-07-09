# Packing Up (task)

```diego
use_namespace(packing_up_demo);

add_ary(content)_arg({int},qty,{str},item);
add_obj(packingBox)_arg({str},code,{content},content);

addto_obj[packingBox]_arg(code)_value(TAV-001)
    ()_arg(content)_arg(qty)_v(2)_arg(item)_v(Lego set 43179);
;


```