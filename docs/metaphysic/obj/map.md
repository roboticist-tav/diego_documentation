# Map




```diego

add_const(ext_wall_width)_v(❬m❭,0.8);
add_const(int_wall_width)_v(❬m❭,0.4);

build_map({2d},{wl},{xy},{boat},❬m❭,primrose2d)
    ()_origin(0,0);
    add_layer(rooms)
        ()_origin(0,0);
        ()_room({bed},bed2)_rect(4.2,3.0)_coord([],[])_calc(0+[ext_wall_width]);
        ()_room({bed},bed1)_rect(3.8,4.0)+coord([x],[y])
            _calc(x,[ext_wall_width]+[bed2.width]+[int_wall_width])
            _calc(y,[ext_wall_width])
        ;
        ()_room({bath},bath)_rect(3.0,1.8)_coord([x],[y])
            _calc(x,[ext_wall_width])
            _calc(y,[ext_wall_width]+[bed2.length]+)
    ;
    
    
    ()_wall(bed2_ext_stern)_rect([w],[l])
        _calc(w,[ext_wall_width]+[bed2.width]+([int_wall_width]/2))
        _calc(l,[ext_wall_width])
        ?_stern();
        ?_exterior();
    ;
    ()_wall(bed2_ext_starb)_rect([w],[l])
        _calc(w,[ext_wall_width])
        _calc(l,[ext_wall_width]+[bed2.length]+([int_wall_width]/2))
        ?_starb();
        ?_exterior();
    ;
    ()_wall(bed1_bed2_int)_rect([w],[l])
        _calc(w,[int_wall_width])
        _calc(h,[bed2.length]+[int_wall_width])
;

    3.783783784

```

<canvas id="rooms">

</canvas>




<a name="declare"></a>
## Declaration

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="declare_assign"></a>
## Declaration & Assignment

<a name="initial"></a>
## Initialisation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `add_(`*`moniker`*`);`<br>

<a name="assign"></a>
## Assignment

<a name="reference"></a>
## Referencing
Referencing a ` ` *object* is achieved with the `with` verb, or the shortened `(`*` `*`)` syntax. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `>_(`*`moniker`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `with_(`*`moniker1`*`,`*`moniker2`*`,`*`…`*`);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `(`*`_moniker`*`);`

<a name="type"></a>
## Typing

<a name="get"></a>
## Getting

<a name="set"></a>
## Setting

<a name="cast"></a>
## Casting

<a name="properties"></a>
## Properties

<a name="example"></a>
## Examples