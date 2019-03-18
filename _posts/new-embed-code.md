title: New code in Publish survey dialog
date: 2014-01-06

Happy new year. We have now updated the code provided by the Publish dialog. The new code looks like:

```
<script type="text/javascript">
	(function(s,u,r,v,e,y){e=window;y=document;y.write('<div id="'+u+'"/>');e[s]={surveyId:r,containerId:u};
	v=y.createElement('script');v.async=1;v.src='//overresponse.com/scripts/respondant/respondant.js';
	y.getElementsByTagName('head')[0].appendChild(v);})('ORSettings', 'ORClientContainer', '517b047386fc3fba190000e2');
</script>
```

The first thing to note is that now the code is minified by default. This is with the idea that someone will simply copy and paste the code on their pages. Of course, this ignores all the options that are available [docs.overresponse.com](http://docs.overresponse.com).

The new code has some other good things too:

1. It will load asynchrously.
2. It will write a container. Please note that although a container Id is provided, it will write a `div` element with that id.

In adition, the publish page now has the option to sample the survey to a fraction of your sites visitors. This is very direct: you select how many of your users want to show the survey to, and the dialog will wrap the code so that only selected users (by a `Math.random` clause) will see the survey.

For instance, if you select '6% of visitors', the code for the same survey will look like:

```
<script type="text/javascript">
if(Math.random()<0.06){(function(s,u,r,v,e,y){e=window;y=document;y.write('<div id="'+u+'"/>');e[s]={surveyId:r,containerId:u};
...
</script>
```

