<%*
await tp.file.move("/content/Unpublished Research/" + tp.file.title);
let title = tp.file.title;
let firstname = "";
let secondname = "";
let name = "";
if (title.startsWith("Untitled")) {
firstname = await tp.system.prompt("First Name:");
secondname = await tp.system.prompt("Surname Name:");
name = firstname + "-" + secondname;
title = await tp.system.prompt("Publication Title (keep this short): ");
await tp.file.rename(firstname + " " + secondname + " - " + title);
}
%>
 #unpublished-research #<% name.toLowerCase() %>   add any other tags that are relevant e.g. developmental, forensic, autism etc. (use # and then type any tag you want without a space after the #)
### Abstract 

