# 格式化剪贴板的内容
```applescript
-- 获取剪贴板内容

set clipboardText to the clipboard

  

-- 删除方括号及其内容

set modifiedText to deleteBracketContent(clipboardText)

  

-- 最终格式：[](docs/allNote/Java基础.md#什么是继承？)

set modifiedText2 to modifiedText

  

  

  

-- 删除方括号及其内容的函数

on deleteBracketContent(sourceText)

    set openBracket to offset of "[" in sourceText

    set closeBracket to offset of "]" in sourceText

    -- 如果找到了方括号，删除它们及其内容

    if openBracket is not 0 and closeBracket is not 0 then

        set sourceText to text (closeBracket + 1) thru -1 of sourceText

    end if

    return sourceText

end deleteBracketContent

  

  

-- 替换 "docs" 为你想要的字符串，这里用 "replaced" 作为示例

set modifiedText3 to replaceText("docs/", "", modifiedText2)

  

-- 要求用户输入

set userInput to text returned of (display dialog "请输入：" default answer "" buttons {"OK"} default button "OK")

  

-- 将用户输入放到替换后的文本的方括号[java基础]内

set finalText to "[" & userInput & "]" & modifiedText3

  

-- 将最终文本写回剪贴板

set the clipboard to finalText

  

tell application "System Events"

        keystroke "v" using command down

end tell

  

-- 替换函数

on replaceText(find, replace, sourceText)

    set text item delimiters to find

    set sourceText to text items of sourceText

    set text item delimiters to replace

    set sourceText to "" & sourceText

    set text item delimiters to ""

    return sourceText

end replaceText
```
