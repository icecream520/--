# VOID ELEMENTS & BREAKS #void元素与空格
ELEMENTS WE WILL LOOK AT
Handling breaks <br> <wbr> <hr>
## VOID ELEMENTS ##
All elements we have seen so far have this structure:
<start_tag> . . . </end_tag>
Some elements do not have any content
These are called 'void elements'
They must not use an end tag//void元素不能使用结束符号
## A VOID ELEMENT WE HAVE ALREADY SEEN ##
<meta name="author" content="David Rossiter">
Void elements may or may not have attributes
## SOME OTHER VOID ELEMENTS ##
Handling multimedia <img> - before
Handling forms <input> - later
Handling breaks <br> <wbr> <hr> - now
    <p>
    My favourite word is supercalifragilisticexpialidocious. It comes
    from the movie 'Mary Poppins' and is hard to spell correctly.
    </p>
    <p>
    My favourite word is supercalifragilisticexpialidocious.<br>It comes
    from the movie 'Mary Poppins' and is hard to spell correctly.
    </p>
    <p>
    My favourite word is supercalifragilistic<wbr>expialidocious. It comes
    from the movie 'Mary Poppins' and is hard to spell correctly.
    </p>
    <p>
    My favourite word is supercalifragilisticexpialidocious.<hr>It comes
    from the movie 'Mary Poppins' and is hard to spell correctly.
    </p>
    //<br>单纯换行<wbr>省略接下来的内容<hr>要显示的内容上面有分割线
