<%* 
let link_path = await tp.system.prompt("Link path");
let heading = await tp.system.prompt("Heading");
let display_text = await tp.system.prompt("Display text");
tR += `[[${link_path}#${heading}|${display_text}]]`
%>
