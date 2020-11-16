# API Documentation
#     1) GetPlayer
Example:
local function getplayer()
  for i = 0, 64 do
     local e = entitylist.get_player_by_index(i)
     if e ~= nil and e:get_alive() then
       client.log("index " .. tostring(i) .. " alive" )
     end
  end
end
client.add_callback("on_createmove", getplayer)

Types:
get_index - returns entity index (int)
get_dormant - returns dormant state (true/false)
get_team - returns team number (int)
get_alive - returns entitie's lifestate (true/false)
get_velocity - returns entitie's velocity (vector)
get_origin - returns entitie's abs origin (vector)
get_angles - returns entitie's eye angles (vector)
get_hitbox_position(i) - returns entitie's hitbox position (vector)
has_helmet - returns entitie's helmet exist (true/false)
has_heavy_armor - returns entitie's heavy armor exist (true/false)
is_scoped - returns entitie's scoped state (true/false)
get_health - returns entitie's helath (int)

#     2) LocalPlayer
Example:
local function localplayer()
  local lc_player = entitylist.get_local_player()
  local index = lc_player:get_index()
end

Types:
get_index - returns entity index (int)
get_dormant - returns dormant state (true/false)
get_team - returns team number (int)
get_alive - returns entitie's lifestate (true/false)
get_velocity - returns entitie's velocity (vector)
get_origin - returns entitie's abs origin (vector)
get_angles - returns entitie's eye angles (vector)
get_hitbox_position(i) - returns entitie's hitbox position (vector)
has_helmet - returns entitie's helmet exist (true/false)
has_heavy_armor - returns entitie's heavy armor exist (true/false)
is_scoped - returns entitie's scoped state (true/false)
get_health - returns entitie's helath (int)

client.add_callback("on_createmove", localplayer)
#     3) SetProp
Example:
local lc_player = entitylist.get_local_player()
lc_player:set_prop_bool("CBaseEntity", "m_bSpotted", true)

Types:
set_prop_int
set_prop_float
set_prop_bool
#     4) SetBool, SetInt, SetFloat
Example:
menu.set_bool("Ragebot.enable", true)
menu.set_int("Ragebot.fov", 180)
menu.set_float("Esp.asus_props_amount", 0.5)
