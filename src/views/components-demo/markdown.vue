<template>
  <div class="components-container">
                <div class="col-xs-12 col-sm-9 content zx_changebg">
                <div class="panel panel-default change_border">
                    <ul class="list-group panel col-xs-3 col-sm-3 chang_padding_rigth">
                        <div class="panel-heading chang_padding">
                          <input class="panel-title button_shuru" value="输入角色名进行查询"></input>
                        </div>
                        <li>
                            <a href="#demo3" class="list-group-item ">默认管理员</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">代理商角色</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">业务员角色</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">分公司经理</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">业务员角色</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">代理商角色</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">业务员角色</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">分公司经理</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">业务员角色</a>
                        </li>
                        <li>
                            <a href="#demo4" class="list-group-item " data-toggle="collapse">代理商角色</a>
                        </li>
                    </ul>
                    <div class="panel_heading_jiaose col-xs-8 col-sm-8">
                        <h3 class="panel_title_jiaose">默认管理员</h3>
                        <div class="btn-group">
                          <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            添加角色
                          </button>
                          <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            编辑角色
                          </button>
                          <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            复制角色
                          </button>
                          <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            删除角色
                          </button>
                        </div>
                        <ul class="nav nav-tabs changebox">
                          <li role="presentation" class="active"><a href="#">菜单权限</a>

                          </li>
                          <li role="presentation"><a href="#">数据权限</a></li>
                          <li role="presentation"><a href="#">文档权限</a></li>
                          <li role="presentation"><a href="#">用户列表</a></li>
                        </ul>
                    </div>
                </div>
            </div>
  </div>
</template>

<script>
import MarkdownEditor from '@/components/MarkdownEditor'

const content = `
**this is test**

* vue
* element
* webpack

## Simplemde
`

export default {
  name: 'markdown-demo',
  components: { MarkdownEditor },
  data() {
    return {
      content: content,
      html: ''
    }
  },
  methods: {
    markdown2Html() {
      import('showdown').then(showdown => {
        const converter = new showdown.Converter()
        this.html = converter.makeHtml(this.content)
      })
    }
  }
}
</script>


