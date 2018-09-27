## 美好的一天

### php的跳转的方法

<?php
    $url = 'https://mitz1979.github.io/myh5/';
    if(isset($url)){
        header("Location:.$url");
    }else{
      echo "页面不存在！";
    }
?>

### js 跳转页面
<?php
    $url = 'https://mitz1979.github.io/myh5';
    if(isset($url)){
        echo "<script>Location.herf='. $url .'</script>"
    }else{
      echo "页面不存在！";
    }
?>

### html 代码跳转
```html


**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/MITZ1979/myH5/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
