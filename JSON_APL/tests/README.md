# Tests for JSON_APL

Exec: niladic, monadic, dyadic, expression

## Exec refactor
Implement tests before doing refactor

```APL
 Exec←{
     9≠⎕NC'⍵':⍎⍵
     val←0<⍵.⎕NC'Left' 'Function' 'Right'
     ~∨/val:'No function or arguments provided'⎕SIGNAL 11
     Join←⊃(⊣,' ',⊢)/
     expr←val/'''Left''' 'Function' '''Right'''
     APL.⍎Join(APL.⍎)Join⍣{1=≡⍺}expr
 }
```