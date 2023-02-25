# oh-my-posh-configuration
## my oh my posh configuration
---

'''json
{
  "$schema": "https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/schema.json",
  "final_space": true,
  "version": 2,
  "blocks": [
    {
      "alignment": "left",
      "type": "prompt",
      "segments": [
        {
          "type": "os",
          "style": "diamond",
          "powerline_symbol": "",
          "invert_powerline": false,
          "foreground": "#26C6DA",
          "background": "#546E7A",
          "leading_diamond": "\ue0b6",
          "trailing_diamond": "\ue0b0",
          "properties": {
            "postfix": "  "
          }
        },
        {
          "type": "session",
          "background": "#00897b",
          "foreground": "#ffffff",
          "template": " {{ .UserName }} ",
          "style": "diamond",
          "leading_diamond": "<transparent,background>\ue0b0</>",
          "trailing_diamond": "\ue0b0"
        },
        {
          "type": "path",
          "background": "#1478DB",
          "foreground": "#000000",
          "leading_diamond": "<transparent,background>\ue0b0</>",
          "trailing_diamond": "\ue0b0",
          "style": "diamond",
          "properties": {
            "style": "mixed"
          }
        },
        {
          "type": "git",
          "background": "#3AD900",
          "background_templates": [
            "{{ if or (.Working.Changed) (.Staging.Changed) }}#FFC600{{ end }}",
            "{{ if and (gt .Ahead 0) (gt .Behind 0) }}#FFCC80{{ end }}",
            "{{ if gt .Ahead 0 }}#B388FF{{ end }}",
            "{{ if gt .Behind 0 }}#B388FF{{ end }}"
          ],
          "foreground": "#000000",
          "leading_diamond": "<transparent,background>\ue0b0</>",
          "properties": {
            "fetch_stash_count": true,
            "fetch_status": true
          },
          "style": "diamond",
          "trailing_diamond": "\ue0b0"
        }
      ]
    },
    {
      "type": "newline"
    },
    {
      "alignment": "left",
      "type": "prompt",
      "segments": [
        {
          "foreground": "#D4E157",
          "foreground_templates": ["{{ if gt .Code 0 }}#FF5252{{ end }}"],
          "properties": {
            "always_enabled": true
          },
          "style": "plain",
          "template": " {{ if gt .Code 0 }}\uf00d{{ else }}\uf42e{{ end }}\u276f",
          "type": "exit"
        }
      ]
    }
  ]
}
'''
