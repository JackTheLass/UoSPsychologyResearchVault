<%*
let title = tp.file.title;
name = await tp.system.suggester(["David Martin", "Phoebe Usher", "Rebecca Owens"], ["David Martin", "Phoebe Usher", "Rebecca Owens"], true, "Name: ");
date = await tp.system.prompt("Publication Date:");
title = await tp.system.prompt("Publication Title (keep this short): ");
filename = "/content/Published Research/" + name + "/" + title + " - (" + date + ")";
await tp.file.move(filename);
-%>
<% "---" %>
Date: <% tp.file.creation_date("DD-MM-YYYY") %>
Time: <% tp.file.creation_date("HH:mm") %>
Author: <% name %>
Publication title: <% title %>
Publication Date: <% date %>
Tags: published-research, <% name.replace(/ /g, '-') %>, 
<% "---" %>
# Abstract



##### Reference 

