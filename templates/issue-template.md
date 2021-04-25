---
layout: default
title: {{.Repository.Name}}
parent: {{.Organization.Name}}
grand_parent: Issues
has_children: false
permalink: /issues/{{.Organization.Github}}/{{.Repository.Name}}
---

# {{.Repository.Name}}

You can clone this repo on <span class="fs-3">[GitHub]({{.Repository.Link}}){: .btn .mr-4 }</span>

{{range .Issues}}
<div class="code-example" markdown="1">
    <table>
        <tr>
            <td>
                Issue [#{{.Number}}]({{.URL}})
            </td>
            <td>
                <b>
                    {{.Title}}
                </b>
            </td>
        </tr>
        <tr>
            <td>
                {{range .Labels}}{{.Name}}{: .label-grey }{{end}}
            </td>
            <td>
                {{.Body}}
            </td>
        </tr>
    </table>
    <div class="right-align">
        Created At {{.CreatedAt}}
    </div>
</div>
{{end}}