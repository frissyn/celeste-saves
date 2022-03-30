#!/usr/bin/env ruby

$name = "docs/savedata.md"
$target = "docs/savedata_abc.md"

r = File.open($name).read
header, content = r.split(".\n")[0], r.split("\n###")

content = content.sort { |a, b| a <=> b }

File.write($target, header << ".\n\n###" << content.join("\n###"))
