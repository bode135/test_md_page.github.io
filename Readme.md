# Markdown���ɾ�̬��վ

> Markdown����wiki�ĵ����ľ�̬��վ, һ�����ڽ̳̻���API�ĵ�.

## Ч��ͼ

![image-20210501210147517](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20210501210147517.png)



## ��װmkdocs

>  �ο��̳�:
>
> - [�ٷ��ĵ�](https://www.mkdocs.org/)
> - [������](https://www.dazhuanlan.com/2020/02/29/5e5a2db520b20/)
>
> - [ʹ�� mkdocs �Զ�����wiki�ĵ�](https://blog.csdn.net/freewebsys/article/details/79218294)

```
pip install mkdocs
```

## �Զ�����

> �ٷ�Ĭ��������һ���ܴ��ȱ��, ����Ĭ�ϵ������Ǻ����.  
>
> �ѵ�������Ϊ��������(`theme: readthedocs`), �����ļ������ɵĶ༶Ŀ¼�޷��Զ�����.  
>
> ��������Ҫ:
>
> - �ļ���:
>   - �ĵ�1.md
>   - �ĵ�2.md
>
> ���ֱ���ʹ��`material`����

- ����ѡ��

  - ��װ: `pip install mkdocs-material`
  - ����: ��`mkdocs.yml`��д��`theme: material`

- ��`mkdocs.yml`�������Զ���css��ʽ�ĵ�`extra_css`�ĵ�ַ`extra_css: extra.css`

- �����ĵ�`mkdocs.yml`���հ�:

  ```
  site_name: py�̳�
  
  theme: material
  
  pages:
      - ��ҳ: index.md
      - User Guide:
          - ����: about.md
          - haha:
              - �ļ�222: source/222.md
              - �ļ�333: source/333.md
      - '������?����!': 'https://www.baidu.com/'
  
  extra_css:
      - extra.css
  ```

