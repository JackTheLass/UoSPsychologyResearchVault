---

---
<%*
await tp.file.move("/content/Research Interests/" + tp.file.title);
let title = tp.file.title;
let firstname = "";
let secondname = "";
let name = "";
if (title.startsWith("Untitled")) {
firstname = await tp.system.prompt("First Name:");
secondname = await tp.system.prompt("Surname Name:");
name = firstname + "-" + secondname;
await tp.file.rename(tp.file.creation_date("DD-MM-YYYY HH") + "h" + tp.file.creation_date("mm") + " - " + firstname + " " + secondname);
}
%>
 #research-interest #<% name.toLowerCase() %> Remember to tag other interests here too e.g. developmental, forensic, autism etc. (use # and then type any tag you want without a space after the #)

Leave a little note here about what interests you!