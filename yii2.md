# Yii2

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
                <?php $form = ActiveForm::begin(['id' => 'contact-form']); ?>
                    <?= $form->field($model, 'firstname')->textInput(['autofocus' => true]) ?>
                    <?= $form->field($model, 'lastname') ?>
                    <?= $form->field($model, 'age') ?>
                    <?= $form->field($model, 'birthdate') ?>
                    <div class="form-group">
                        <?= Html::submitButton('send', ['class' => 'btn btn-primary']) ?>
                    </div>
                <?php ActiveForm::end(); ?>
            </div>
        </div>
    </div>
    ```

11. Based on the given Yii2 code template snippet, replace the two placeholders in the configuration to add a URL rule for the country controller so that the country data can be accessed and manipulated with pretty URLs and meaningful HTTP verbs.
You are not allowed to add additional lines to the code.

    *vgl. [Docs](https://www.yiiframework.com/doc/guide/2.0/en/rest-quick-start#:~:text=can%20be%20accessed%20and%20manipulated%20with%20pretty%20URLs%20and%20meaningful%20HTTP%20verbs.)* 
    (alternativ: [PrettyUrl-Docs](https://www.yiiframework.com/doc/guide/2.0/en/runtime-routing#using-pretty-urls))

    ```php
    'urlManager' => [
        'enablePrettyUrl' => true,
        'enableStrictParsing' => true,
        'showScriptName' => false,
        'rules' => [
            ['class' => 'yii\rest\UrlRule', 'controller' => 'country'],
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


## Zusatzfragen

-   The following diagramm shows the static structure of a Yii2 application. Fill in the re-bordered boxes with the missing terms.

    [![](https://www.yiiframework.com/doc/guide/2.0/en/images/application-structure.png)](https://www.yiiframework.com/doc/guide/2.0/en/structure-overview)

    - entry scripts: they are PHP scripts that are directly accessible by end users. They are responsible for starting a request handling cycle.
    - applications: they are globally accessible objects that manage application components and coordinate them to fulfill requests.
    - application components: they are objects registered with applications and provide various services for fulfilling requests.
    - modules: they are self-contained packages that contain complete MVC by themselves. An application can be organized in terms of multiple modules.
    - filters: they represent code that need to be invoked before and after the actual handling of each request by controllers.
    - widgets: they are objects that can be embedded in views. They may contain controller logic and can be reused in different views.

<br>

- Based on the given code template complete the code to implement a Yii2 RESTful Web Services controller (RWSC) The RWSC should expose the country model class via RESTful actors. You are not allowed to add additional lines to the code.

    *Angabe unvollständig; 
    vgl. [Docs](https://www.yiiframework.com/doc/guide/2.0/en/rest-quick-start)*
    ```php
    // app\controllers\CountryController

    namespace app\controllers;

    use yii\rest\ActiveController;

    class CountryController extends ActiveController
    {
        public $modelClass = 'app\models\Country';
    }
    ```

    ```php
    // app\config\web.php

    'urlManager' => [
        'enablePrettyUrl' => true,
        'enableStrictParsing' => true,
        'showScriptName' => false,
        'rules' => [
            ['class' => 'yii\rest\UrlRule', 'controller' => 'country'],
        ],
    ]
    ```

- Based on the given Yii2 configuration template snippet, replace the three placeholder in the configuration to add  module country to your Yii2 application. You are not allowed to add additional lines to the code.

    *Angabe unvollständig*
    ```php
    ???
    ```

- The following source code shows  the declaration of actionAbout that should display the about page. What must be the return value?

    *Angabe unvollständig; vgl. [Docs](https://www.yiiframework.com/doc/guide/2.0/en/start-hello)*
    ```php
    // app\controllers\SiteController.php

    /**
     * Displays about page.
     *
     * @return string
     */
    public function actionAbout()
    {
        return $this->render('about');
    }
    ```

- A Yii2 Controller CID belongs to module MID. What is the route format for action AID?

    *vgl. [Docs](https://www.yiiframework.com/doc/guide/2.0/en/structure-controllers#:~:text=ModuleID/ControllerID/ActionID)*
    ```txt
    MID/CID/AID
    ```

- What is the name of the default controller of the Yii2 console application?

    *vgl [Docs](https://www.yiiframework.com/doc/guide/2.0/en/structure-controllers#:~:text=while%20for%20console%20applications,%20it%20is%20help.)*
    ```php
    HelpController
    ```

- Which Yii2 component is used to collect information about a user request and resolve it into a route?

    *vgl. [Docs](https://www.yiiframework.com/doc/guide/2.0/en/structure-application-components#:~:text=For%20example%2C%20the%20request%20component,you%20can%20perform%20database%20queries.)*

    ```txt
    the request component
    ```
    

- You are about to create a new Yii2 module. Which public method of the module class contains the code initializing the modules properties?

    ```php
    init()
    ```

- Cross-site request forgery is also known as?
    ```txt
    Session Riding || One-Click-Attack
    ```