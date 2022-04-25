# 命令索引

若要查看所有 Nushell 命令, 可以执行 [`help commands`](/book/commands/help.md)。

译注：本页内容由于是从源码生成的暂不支持国际化，大家还是先看英文版的凑合下吧。

<script>
  export default {
    computed: {
      commands() {
        return this.$site.pages
          .filter(p => p.path.indexOf('/book/commands/') >= 0)
          .sort((a,b) => (a.title > b.title) ? 1 : ((b.title > a.title) ? -1 : 0));
      }
    }
  }
</script>

<table>
  <tr>
    <th>Command</th>
    <th>Description</th>
  </tr>
  <tr v-for="command in commands">
   <td><a :href="command.path"><code>{{ command.title }}</code></a></td>
   <td style="white-space: pre-wrap;">{{ command.frontmatter.usage }}</td>
  </tr>
</table>