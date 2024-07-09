<%*
let title = tp.file.title;
let name = "";
if (title.startsWith("Untitled")) {
name = await tp.system.suggester(["David Martin", "Phoebe Usher", "Rebecca Owens"], ["David Martin", "Phoebe Usher", "Rebecca Owens"], true, "Name: ");
filetitle = tp.file.creation_date("DD-MM-YYYY HH") + "h" + tp.file.creation_date("mm")
filename = "/content/Research Interests/" + name + "/" + filetitle
await tp.file.move(filename);
await tp.file.rename(filetitle);
}
-%>
<% "---" %>
Date: <% tp.file.creation_date("DD-MM-YYYY") %>
Time: <% tp.file.creation_date("HH:mm") %>
Author: <% name %>
Tags: research-interests, <% name.replace(/ /g, '-') %>, 
<% "---" %>
Add any other tags that are relevant e.g. developmental, forensic, autism etc. (use # and then type any tag you want without a space after the #)
# Research Interest
