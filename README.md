# _UIA_getVars
func _UIA_action($obj_or_string, $strAction, $p1=0, $p2=0, $p3=0)      local $tPattern     local $x, $y ;~  local $objElement     local $oElement  ;~ If we are giving a description then try to make an object first by looking from repository ;~ Otherwise assume an advanced description we should search under one of the previously referenced elements at runtime     if isobj($obj_or_string) or IsObj(_UIA_getVar("RTI." &amp; $obj_or_string)) Then ; check if obj_or_string is an object, or if it is stored in the RTI         If isobj($obj_or_string) Then ; if object, use it             $oElement = $obj_or_string             $obj = $obj_or_string         Else ; if RTI.object, use that             $oElement = _UIA_getVar("RTI." &amp; $obj_or_string)             $obj = _UIA_getVar("RTI." &amp; $obj_or_string)         EndIf     else ; rest of function....
