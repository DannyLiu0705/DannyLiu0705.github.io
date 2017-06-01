---
title: Symfony3 表单组件Radio
date: 2017-05-17 16:45:40
tags:
---
使用了PHP Symfony3的表单,总结一下Radio组件的使用,因为本人在使用的时候查阅了很多文档,一直没有详细的资料,所以在此记录一下.

## PHP文件:
```bash
public function buildForm(FormBuilderInterface $builder, array $options)
{
  $builder
    ->add('moneyType', ChoiceType::class, array(
      'choices' => array(
        '元' => Money::MONEY_RMB, //key 是页面显示的提示, value是选中的值
        '美元' => Money::MONEY_DOLLER
      ),
      'expanded' => true,
      'multiple' => false
  ))
}
```
## html文件:
<!-- more -->
```bash
{{ form_start(form, { 'attr': { 'class': 'form-horizontal'} }) }}
<div class="col-sm-6">
    {{ form_errors(form.moneyType) }}
    <span class="col-sm-3">
        {{ form_widget(form.moneyType[0], {'attr': {'class': 'flat-red'}}) }}
        {{ form_label(form.moneyType[0]) }}
    </span>
    <span class="col-sm-3">
        {{ form_widget(form.moneyType[1], {'attr': {'class': 'flat-red'}}) }}
        {{ form_label(form.moneyType[1]) }}
    </span>
</div>
{{ form_end(form) }}
```

## 更多使用参考[Symfony](http://symfonychina.com/) 官方网站。
