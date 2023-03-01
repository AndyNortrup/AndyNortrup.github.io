---
date: 2023-03-01T00:00:00Z
title: Hashtag strings in Hugo
tags:
  - Technology
  - Hugo
categories: Technology
alisases:
  -
  - ''
---
I did a fun bit of Hugo templating today that seemed worth sharing. I was previously generating my list of hashtags to apply to a social post inside of my Zapier workflow. I'd pull the list of tags then manipulate them into a single string and add the \# symbol.

Today I realized that this would be much simpler to do in Hugo as part of my JSON output. It came out like this:

{{< highlight "md" >}}"hashtags" (delimit
            (apply (apply .Params.tags "replaceRE" "\\s" "" ".")
                    "print"
                    "#" ".")
                " "){{< /highlight >}}

Two apply statements might be overkill, but it works. I needed to do three things:

1. Title case the words so we get ProductManagement, rather than Productmanagement or productmanagement.
2. Remove the spaces.
3. Converts the list to a single string that I can just plop into a post.

Now I have one field that I can put into a post. I find that zero code workflows are best when simplest. Doing variable manipulation with them is never elegant.