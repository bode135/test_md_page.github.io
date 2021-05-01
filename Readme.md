# Markdown生成静态网站

> Markdown生成wiki文档风格的静态网站, 一般用于教程或者API文档.

## 效果图

![image-20210501210147517](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20210501210147517.png)



## 安装mkdocs

>  参考教程:
>
> - [官方文档](https://www.mkdocs.org/)
> - [简单入门](https://www.dazhuanlan.com/2020/02/29/5e5a2db520b20/)
>
> - [使用 mkdocs 自动生成wiki文档](https://blog.csdn.net/freewebsys/article/details/79218294)

```
pip install mkdocs
```

## 自定义风格

> 官方默认主题有一个很大的缺陷, 就是默认导航栏是横向的.  
>
> 把导航栏改为左侧竖向后(`theme: readthedocs`), 根据文件夹生成的多级目录无法自动缩进.  
>
> 例如我想要:
>
> - 文件夹:
>   - 文档1.md
>   - 文档2.md
>
> 这种必须使用`material`主题

- 主题选择

  - 安装: `pip install mkdocs-material`
  - 配置: 在`mkdocs.yml`中写入`theme: material`

- 在`mkdocs.yml`中配置自定义css样式文档`extra_css`的地址`extra_css: extra.css`

- 配置文档`mkdocs.yml`最终版:

  ```
  site_name: py教程
  
  theme: material
  
  pages:
      - 首页: index.md
      - User Guide:
          - 关于: about.md
          - haha:
              - 文件222: source/222.md
              - 文件333: source/333.md
      - '有疑问?点我!': 'https://www.baidu.com/'
  
  extra_css:
      - extra.css
  ```

