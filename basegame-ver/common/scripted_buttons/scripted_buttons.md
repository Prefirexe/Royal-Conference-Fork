UI can obtain a datamodel with all the scripted buttons via "[JournalEntry.GetScriptedButtons]". Each scripted button
can be referred to via "ScriptedButton".
Scripted buttons' properties can be accessed by UI via

- [ScriptedButton.GetName] -> provides a string
- [ScriptedButton.GetDesc] -> provides a string
- [ScriptedButton.GetEffectDesc] -> provides a string
- [ScriptedButton.IsVisible] -> provides a bool
- [ScriptedButton.IsPossible] -> provides a bool
- [ScriptedButton.ExecuteEffect] -> provides nothing, executes the effect


    scripted_button_key = {
      name = "LOC_KEY"
      desc = "LOC_KEY_DESC"

          visible = { always = yes }

          #Country scope
          ai_chance = {
              base = 0
              modifier = {
                  trigger = { bureaucracy > 0 }
                  add = 5
              }
          }

          possible = {
              not = {
                  has_variable = my_cool_var
              }
          }

          effect = {
              set_variable = my_cool_var
          }
      }
