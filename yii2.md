# Fragen zu Yii2

9. Refer to the Yii2 Request Lifecycle. Drag the right keywords onto the red-bordered boxes with the missing terms.

    [![Request Handling Lifecycle aus den Docs](https://www.yiiframework.com/doc/guide/2.0/en/images/request-lifecycle.png)](https://www.yiiframework.com/doc/guide/2.0/en/runtime-overview)

10. The following PHP code shows the view of the Yii2 advanced template's contact form.
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
                <?php $form = ActiveForm::begin(['id' =>    'contact-form']); ?>
                    <?= $form->field($model, 'firstname')->textInput   (['autofocus' => true]) ?>
                    <?= $form->field($model, 'lastname') ?>
                    <?= $form->field($model, 'age') ?>
                    <?= $form->field($model, 'birthdate') ?>
                    <div class="form-group">
                        <?= Html::submitButton('Submit', ['class' =>    'btn btn-primary', 'label' => 'send']) ?>
                    </div>
                <?php ActiveForm::end(); ?>
            </div>
        </div>
    </div>
    ```

11. Based on the given Yii2 code template snippet, replace the two placeholders in the configuration to add a URL rule for the country controller so that the country data can be accessed and manipulated with pretty URLs and meaningful HTTP verbs.
You are not allowed to add additional lines to the code.

    ```php
    'urlManager' => [
        'enablePrettyUrl' => true
        'enableStrictParsing' => true,
        'showScriptName' => false,
        'rules' => [
            ['class' => 'Country', 'defaults' => 'model', 'route' => 'site/CountryController',?],
        ],
    ]
    ```

12. Your site controller needs a new action for rendering page "FollowMe". What is the correct action name following the Yii2 naming conventions?

    ```txt
    actionFollowMe
    ```

13. Your site needs a new controller "games" for rendering the games page. What is the correct controller name following the Yii2 naming conventions?

    ```txt
    GamesController
    ```

14. What is the name of the default controller of a Yii2 website?

    ```txt
    SiteController
    ```

15. Which Yii2 component is responsible for routing Web request?

    ```txt
    UrlManager
    ```

16. You are about to create a new Yii2 module. From which class should the unique module class extend?

    ```txt
    \yii\base\Module
    ```

17. Which of the following statements are true about Yii2 ? (Choose all that apply.)

    - [ ] Yii2 implements the MVVM (Model-View-Viewmodel) architectural pattern.
    - [ ] Yii2 implements the Yii2 implements the Cross-Site-Request-Forgery (CSRF) component pattern.
    - [x] Yii2 has a component-based architecture.
    - [x] Yii2 is suitable for developing RESTful Web services.
    - [ ] Yii2 implements the Component architectural pattern.
    - [x] Yii2 implements the MVC (Model-View-Controller) architectural pattern.

18. What represents the following Yii2 code snippet?

    ```php
    <?php

    use yii\helpers\Html;

    $this->title = 'FollowMe';
    $this->params['breadcrumbs'][] = $this->title;
    ?>

    <div class="site-followme">
     <h1><?= Html::encode($this->title) ?></h1>
     <p>This is the FollowMepage. You may modify the following file to customize its content:</p>
     <code><?= __FILE__ ?></code>
    </div>
    ```

    - [x] a view
    - [ ] a controller
    - [ ] a model
