<%*
let title = tp.file.title;
let name = "";
name = await tp.system.suggester(["David Martin", "Phoebe Usher", "Rebecca Owens"], ["David Martin", "Phoebe Usher", "Rebecca Owens"], true, "Name: ");
title = await tp.system.prompt("Publication Title (keep this short): ");
filename = "/content/Published Research/" + name + "/" + title + 
await tp.file.move(filename);
-%>
<% "---" %>
Date: <% tp.file.creation_date("DD-MM-YYYY") %>
Time: <% tp.file.creation_date("HH:mm") %>
Author: <% name %>
Publication title: <% title %>
Tags: unpublished-research, <% name.replace(/ /g, '-') %>, 
<% "---" %>
# Abstract
