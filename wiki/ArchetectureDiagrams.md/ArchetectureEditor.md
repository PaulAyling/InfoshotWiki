Editor Folder Component Diagram

userFunctions
 ./supportingFunctions
 
|userFunctions|
|JSONData or Db connection|
Editor
 Chapter
  ComponentWrapper
   Draggable
    Header(ModifyChapter)
     Droppable
      Contents
       {Page}    
Page
 ComponentWrapper
	Draggable
   Header(ModifyPage)
    Droppable
     VerticalList
      {Paragraph}	
Paragraph
 ComponentWrapper
  Draggable
   Header(ModifyParagraph)
    Droppable
     VerticalList
      {Words}
Words
 ComponentWrapper
  Draggable
   Header(ModifyParagraph)
    Droppable
     VerticalList

modifyChapter, ModifyPage, 
ModifyWords (all similar)