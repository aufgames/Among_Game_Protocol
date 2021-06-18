# `0x09` SetHat

This message is sent by a client's [`PlayerControl`](../05_innernetobject_types/04_playercontrol.md) object when joining a game or when customizing their [`Hat`](../01_packet_structure/06_enums.md#hat) in the lobby.

> **Note**: This message is sent to and from all clients in a game via [`0x05` GameData](../02_root_message_types/05_gamedata.md).

| Type | Name | Description |
| --- | --- | --- |
| `packed uint32` | Hat ID | The ID of the player's new [`Hat`](../01_packet_structure/06_enums.md#hat) |

<details>
    <summary>Click here to view an example packet</summary>

```
01              # Reliable packet
003d            # Nonce
210005          # Hazel message (tag of 0x05 = GameData)
    d3503f8a    # Game ID: -1975562029 (REDSUS)
    030002      # Hazel message (tag of 0x02 = RPC)
        4b      # Sender (PlayerControl) Net ID: 75
        09      # RPC Call ID: 9 (SetHat)
        40      # Hat ID: 64 (MOHAWK)
```
</details>

---

> Previous section: [`0x08` SetColor](08_setcolor.md)<br>
> Next section: [`0x0a` SetSkin](10_setskin.md)
