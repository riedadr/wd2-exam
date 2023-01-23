# Fragen zu Yii2

- Refer to the Yii2 Request Lifecycle. Drag the right keywords onto the red-bordered boxes with the missing terms.

![Request Handling Lifecycle aus den Docs](https://www.yiiframework.com/doc/guide/2.0/en/images/request-lifecycle.png)

- The following PHP code shows the view of the Yii2 advanced template's contact form.
Copy the code to a local file and create the Yii2 view for an Yii2 ActiveForm that shows the input fields:
firstname,
lastname,
age,
birthdate
in this order and a submit button with label "send". Autofocus should be on field "firstname".

```php
<?php

/* @var $this yii\web\View */
/* @var $form yii\bootstrap\ActiveForm */
/* @var $model \frontend\models\ContactForm */

use yii\helpers\Html;
use yii\bootstrap\ActiveForm;
use yii\captcha\Captcha;

$this->title = 'Contact';
$this->params['breadcrumbs'][] = $this->title;
?>
<div class="site-contact">
    <h1><?= Html::encode($this->title) ?></h1>
    <p>Please give us your data</p>
    <div class="row">
        <div class="col-lg-5">
            <?php $form = ActiveForm::begin(['id' => 'contact-form']); ?>
                <?= $form->field($model, 'firstname')->textInput(['autofocus' => true]) ?>
                <?= $form->field($model, 'lastname') ?>
                <?= $form->field($model, 'age') ?>
                <?= $form->field($model, 'birthdate') ?>
                <div class="form-group">
                    <?= Html::submitButton('Submit', ['class' => 'btn btn-primary', 'label' => 'send']) ?>
                </div>
            <?php ActiveForm::end(); ?>
        </div>
    </div>
</div>

```