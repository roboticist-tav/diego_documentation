# Puff



## Objects / Child Objects

The parent object is the `puff` which acts as a classifications of six objects where are departmentalised upon their range.

| `{obj}`| range  | examples |
|---|---|---|---|
| `mist`  | < 1m | _wired systems_   | `add_puff({moniker|uuid})_type(mist);`<br>`add_mist({moniker|uuid});` |
| `fog` | < 10m | RFID | `add_puff({moniker|uuid})_type(fog);`<br>`add_fog({moniker|uuid});` |
| `smog` | < 100m | Wi-Fi, Bluetooth, BLE, Radio  |
| `murk` | < 1km | HaLow |
| `yonder` | 1km + | LPWAN, Cellular |
| `cloud` | _indefinite_ | _(carriers: twitter, slack, discord)_ |

  The `puff` and its six children can be created using the `add_` verb:

### Creation

Direct `add_` creation can be accomplished in a variety of ways.  The parent object, `puff`, can be created with the `add_` verb and will act as a _generic_ _type_^♣^. The children objects of a `puff` can be created via `{puff_type}`^♣^. Also, the `puff` children can be created with the `add_` verb^♣^:
```Diego
add_puff({moniker|uuid}); 
add_puff({moniker|uuid})_type({puff_type});
add_{obj}({moniker|uuid}); 
```

Where:
| `{puff_type}`, `{obj}` | commands |
|---|---|
| `mist` | `add_puff({moniker|uuid})_type(mist);`<br>`add_mist({moniker|uuid});` |
| `fog` | `add_puff({moniker|uuid})_type(fog);`<br>`add_fog({moniker|uuid});` |
| `smog` | |
| `murk` | |
| `yonder` |
| `cloud` | |

The `puff` children can also be assembled^♣^:
```Deigo
add_puff({moniker|uuid});

add_mist({moniker|uuid});
add_fog({moniker|uuid});
add_smog({moniker|uuid});
add_murk({moniker|uuid});
add_yonder({moniker|uuid});
add_cloud({moniker|uuid});

with_puff({moniker|uuid})_mist({moniker|uuid});
with_puff({moniker|uuid})_fog({moniker|uuid});
with_puff({moniker|uuid})_smog({moniker|uuid});
with_puff({moniker|uuid})_murk({moniker|uuid});
with_puff({moniker|uuid})_yonder({moniker|uuid});
with_puff({moniker|uuid})_cloud({moniker|uuid});
```

♣ All the above commands, without any discrimination, will create their `puff` for anyone who hears the command, then anyone who hears the command will automatically be nodes to the `puff`.  Use discrimination postpositions to specify nodes.

## Existence

The `puff` and its children should not be brought into existence without creation. If a _thingy_ finds the existence of a `puff` it will try and find its creation using `with_{puff}({moniker|uuid}_bithof();` for similar syntax^♠^:

```Diego
→ add_puff({moniker|uuid});
→ with_puff({moniker|uuid})_mist({moniker|uuid});
→ with_puff({moniker|uuid})_fog({moniker|uuid});
→ with_puff({moniker|uuid})_smog({moniker|uuid});
→ with_puff({moniker|uuid})_murk({moniker|uuid});
→ with_puff({moniker|uuid})_yonder({moniker|uuid});
→ with_puff({moniker|uuid})_cloud({moniker|uuid});

← with_mist({moniker|uuid})_birthof();
* me_err(c102,existance_with_no_found_creation)_appliedto(mist)_specificto({moniker|uuid};
← with_fog({moniker|uuid})_birthof();
* me_err(c102,existance_with_no_found_creation)_appliedto(fog)_specificto({moniker|uuid};
← with_smog({moniker|uuid})_birthof();
* me_err(c102,existance_with_no_found_creation)_appliedto(smog)_specificto({moniker|uuid};
← with_murk({moniker|uuid})_birthof();
* me_err(c102,existance_with_no_found_creation)_appliedto(murk)_specificto({moniker|uuid};
← with_yonder({moniker|uuid})_birthof();
* me_err(c102,existance_with_no_found_creation)_appliedto(yonder)_specificto({moniker|uuid};
← with_cloud({moniker|uuid})_birthof();
* me_err(c102,existance_with_no_found_creation)_appliedto(cloud)_specificto({moniker|uuid};
```

♠ The creation command and _existence_ commands are without any discrimination, this will create their puff for anyone who hears the command, then anyone who hears the command will automatically be nodes to the puff. Use discrimination postpositions to specify nodes.

Without any reply to the `_bithof` enquiry, the callee will remember commands of the `puff` but not act upon those commands until the respective `add_` verb has been found.  The callee will remember this as an error: `me_err({err_num}, {err_desc})_appliedto({obj|child_obj})_specificto({moniker|uuid})[_forwhat({moniker|uuid})];`.

Since, in this examples, no discimination has been applied, any `thingy` (with knowledge of the 'puff's creation) can respond to the `_birthof()` enquiry even if they are not the creator.

## Solutions

Syntax: `_solut({solut_type}[, {generation}])`

The solution `_solut` postposition

```Diego
add_smog({moniker|uuid})_solut({solut_type}[, {generation}])_protocol({protocol});
```
Where:

| `{solut_type}` | `{generation}` | description  |
|---|---|---|
| `rfid`  | RFID  |
| `wi_fi` | `4`<br>`5`<br>`6`<br>`7`<br>`halow` | |
| `lte-m` | `r`... | |
| `mythings`
|  


## Hijacking Google Chat

Google Chat can be hijacked to provide a communication `cloud` to allow `thingy`s to communicate.  Just as a human, each `thingy` will require a Google account, an email address, and access to the Google Chat API.

As a demonstration/example we have two robots, `alif` and `bahh`.  Each robot knows the credentials (*i.e. where to meet*) of the Google chat room and each others email address.  They are best of friends, _i.e. they know each other_. `alif` will create the `channel` (called _rooms_ in Google Chat) and send an invite to `bahh`.

We will start with `alif`, just going over (for the sake of this demonstration) some _setting-up_ it did as a child...
##### `alif`
```Diego
add_email(alif@diegolang.org)_linkto(google)_me();
```
...and `bahh`...

##### `bahh`
```Diego
add_email(bahh@diegolang.org)_linkto(google)_me();
add_cloud(google_chat)_solut(google_chat)_me();

begin_instruct(listen_on_google_chat);
    add_listener(listen_for_invites_on_google_chat)_appliedto(cloud)_specificto(google_chat)_forwhat(invite) ? with_channel()_specificto()_accept() : exit_instruct(listen_on_google_chat);
    ping_thingy()_cloud(google_chat)_thingy();
end_instruct(listen_on_google_chat);

exec_instruct(listen_on_google)_chat)_me();
```

Now `alif` (and `bahh`) have to set-up their Google Chat connectivity as a `cloud`...
##### `alif`
```Diego
add_cloud(google_chat)_solut(google_chat)_me();
add_channel(diego_test_room_001)_me();
with_cloud(google_chat)_channel(diego_text_room_001)_me();
with_channel(diego_text_room_001)_invite(bahh);

ping_thingy()_cloud(google_chat)_thingy();
pong_robot(alif)_for(bah);
```
...and `bahh`...

##### `bahh`
```Diego
ping_thingy()_cloud(google_chat)_thingy()_for(alif);
pong_robot(alif)_for(bah);
```




channel


fanal - a beacon for guiding ships


funnel <-> fennul
