---
title: التوقيع على نقطة البيع الحديثة بواسطة شهادة توقيع التعليمات البرمجية
description: يشرح هذا الموضوع كيفية التوقيع على نقطة البيع الحديثة بواسطة شهادة توقيع التعليمات البرمجية.
author: mugunthanm
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: e45961cf1ddb385d914b700d03bc95d07de47b68
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2022
ms.locfileid: "8741532"
---
# <a name="sign-mpos-appx-with-a-code-signing-certificate"></a>التوقيع على MPOS appx بواسطة شهادة توقيع التعليمات البرمجية

[!include [banner](../includes/banner.md)]

لتثبيت Modern POS (MPOS)، يجب عليك التوقيع على تطبيق MPOS بشهادة توقيع التعليمات البرمجية من موفر موثوق وتثبيت نفس الشهادة على جميع الأجهزة حيث تم تثبيت MPOS ضمن المجلد الجذر الموثوق به للمستخدم الحالي.

للتوقيع على تطبيق MPOS باستخدام شهادة، استخدم أحد الخيارات التالية في الملف **Retail SDK\\Build tool\\Customization.settings**:

- أضف جزء مهمة الملف الآمن من خطوات إنشاء Azure DevOps وتحميل الشهادة لتأمين مهمة الملف. استخدم متغير مسار إخراج مهمة الملف الآمن كمعلمة في ملف إعدادات التخصيص.

    > [!NOTE]
    > لا تدعم مهمة الملف الآمن شهادة محمية بكلمه مرور. يجب إزالة كلمه المرور قبل تحميل هذه المهمة. بسبب تحميل الشهادة إلى مهمة نظام الملفات الآمنة في Azure، يمكنك إزالة كلمه المرور لهذه الخطوة فقط. ومع ذلك، يجب مناقشه إزالة كلمه المرور مع خبراء الأمان لتحديد ما إذا كان هذا الاجراء هو الاجراء الصحيح لمشروعك. لا تعمل على إزالة كلمة مرور الشهادة للسيناريوهات الأخرى.
- استخدم شهادة موجودة في نظام الملفات. للقيام بذلك، قم بتنزيل أو إنشاء شهادة وضعها في نظام الملفات حيث يتم تشغيل الإصدار. يجب أن يكون لدى المندوب المستضاف من Microsoft أو مستخدم الإصدار حق الوصول إلى هذا المسار والملف.
- استخدم بصمة الإبهام للبحث عن الشهادة في المتجر وسجل دخولك باستخدام تلك الشهادة.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>استخدام مهمة الملف الآمن لتسجيل الدخول إلى تطبيق Universal Windows Platform

> [!NOTE]
> يمكنك أيضًا استخدام Azure Key Vault لتخزين الشهادة واستخدام أداة التوقيع في Azure للتوقيع على ملف Modern POS .appx ومثبتات الخدمة الذاتية. فيما يتعلق بالبرامج النصية لعينة التدفق وللحصول على معلومات إضافية، راجع [إعداد تدفق بناء في Azure DevOps لإنشاء حزم الخدمة الذاتية للبيع بالتجزئة](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

يعد استخدام مهمة الملف الآمن الأسلوب المستحسن لتسجيل الدخول إلى تطبيق Universal Windows Platform (UWP). لمزيد من المعلومات حول التوقيع على الحزم، راجع [تكوين التوقيع على الحزم](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). تظهر هذه العملية في الصورة التالية.

![سير عمل التوقيع على التطبيق MPOS.](media/POSSigningFlow.png)

> [!NOTE]
> تدعم حزمة OOB حاليًا التوقيع على ملف appx فقط، ولم يتم التوقيع على مثبتات الخدمة الذاتية المختلفة مثل MPOIS وRSSU وHWS بواسطة هذه العملية. تحتاج إلى التوقيع عليه يدويًا باستخدام SignTool أو أدوات توقيع أخرى. يجب تثبيت الشهادة المستخدمة للتوقيع على ملف appx في الجهاز حيث تم تثبيت Modern POS.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>الخطوات المطلوبة بتكوين الشهادة للتوقيع في Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>الشهادة في نظام الملفات/الموقع الآمن

قم بتنزيل [DownloadFile task](/visualstudio/msbuild/downloadfile-task) وأضفتها باعتبارها الخطوة الأولى في عملية البناء. تتمثل ميزة استخدام مهمة الملف الآمن في أن الملف يتم تشفيره ووضعه في القرص أثناء الإنشاء بغض النظر عما إذا كان تدفق البناء قد نجح أو فشل أو تم إلغاؤه. يتم حذف الملف من موقع التحميل بعد إتمام عمليه البناء.

1. قم بتنزيل مهمة الملف الآمن وإضافتها باعتبارها الخطوة الأولى في تدفق البناء في Azure. يمكنك تنزيل مهمة الملف الآمن من [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
2. قم بتحميل الشهادة إلى مهمة الملف الآمن وقم بتعيين اسم المرجع ضمن متغيرات الإخراج، كما هو موضح في الصورة التالية.
    > [!div class="mx-imgBorder"]
    > ![مهمة الملف الآمن.](media/SecureFile.png)
3. أنشئ متغيرًا جديدًا في Azure Pipelines عن طريق تحديد **متغير جديد** ضمن علمة تبويب **المتغيرات**.
4. أدخل اسمًا للمتغير في حقل القيمة، على سبيل المثال، **MySigningCert**.
5. احفظ المتغير.
6. افتح الملف **Customization.settings** من **RetailSDK\\BuildTools** وقم بتحديث **ModernPOSPackageCertificateKeyFile** بواسطة اسم المتغير الذي تم إنشاؤه في التدفق (الخطوة 3). على سبيل المثال:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    هذه الخطوة مطلوبة إذا لم تكن الشهادة محمية بكلمة مرور. إذا كانت الشهادة محمية بكلمة مرور، فتابع الخطوات التالية.
 
7. في علامة التبويب **المتغيرات** الخاصة بالتدفق، أضف متغير secure-text جديدًا. عيّن الاسم إلى **MySigningCert.secret** وعيّن قيمة كلمة المرور للشهادة. حدد أيقونة القفل لتأمين المتغير.
8. أضف مهمة **Powershell Script** إلى الدفق (بعد تنزيل الملف الآمن وقبل خطوة البناء). أدخل اسم **العرض** وعيّن النوع على أنه **مضمن**. انسخ والصق ما يلي في قسم البرنامج النصي.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

9. افتح الملف **Customization.settings** من **RetailSDK\\BuildTools** وقم بتحديث **ModernPOSPackageCertificateThumbprint** بواسطة قيمة بصمة إبهام الشهادة.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
للحصول على تفاصيل حول كيفية الحصول على بصمه إبهام الشهادة، راجع [استرداد بصمة إبهام الشهادة](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

 
## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>تنزيل أو إنشاء شهادة للتوقيع على تطبيق MPOS يدويًا باستخدام msbuild في SDK

إذا تم استخدام شهادة تم تنزيلها أو إنشاؤها للتوقيع على تطبيق MPOS، فعليك عندئذٍ تحديث العقدة **ModernPOSPackageCertificateKeyFile** في الملف **BuildTools\\Customization.settings** للإشارة إلى موقع ملف pfx (**$(SdkReferencesPath)\\appxsignkey.pfx**). على سبيل المثال:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

في هذه الحالة، يكون اسم ملف الشهادة **appxsignkey.pfx**، الموجود في المجلد **Retail SDK\\Reference**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>استخدام بصمة إبهام للتوقيع على تطبيق MPOS

إذا كنت تستخدم بصمة الإبهام للتوقيع على تطبيق MPOS، فعليك تثبيت الشهادة محليًا. حدّث قيمة بصمة الإبهام في العقدة **ModernPOSPackageCertificateThumbprint** في الملف **BuildTools\\Customization.settings**.

هذا الخيار سيعمل إذا كان مستخدم البنية مستخدمًا محليًا. ومع ذلك، إذا كنت تستخدم مندوبي Azure DevOps لإنشاء البنية، فقد لا يكون لدى المندوب إذن للوصول إلى مخزن الشهادات لاستخدام شهادة للتوقيع أو أن الشهادة لن تكون مثبتة في جهاز البناء. وفي هذه الحالة، يكون الحل البديل هو تغيير مستخدم البناء إلى مستخدم محلي وتثبيت الشهادة في الصندوق. ومع ذلك، لن يعمل هذا الخيار إذا لم يكن لديك حق الوصول كمسؤول إلى الصندوق.

> [!NOTE]
> إذا تم استخدام الملف pfx. أو خيار مهمة الملف الآمن للتوقيع على التطبيق، فاترك العقدة **ModernPOSPackageCertificateThumbprint** في **Customization.settings** فارغة. إذا تم استخدام خيار بصمه الإبهام، فاترك الخيار **ModernPOSPackageCertificateKeyFile** فارغًا. إذا تم تحديث القيمتين، فستفشل البنية.

### <a name="certification-renewal"></a>تجديد الشهادة

### <a name="renew-a-certificate-from-trusted-ca"></a>تجديد شهادة من مرجع مصدق (CA) موثوق به

اتصل بالمرجع المصدق (CA) من أجل عملية تجديد الشهادة. بالنسبة للشهادة الموثوق بها، لا حاجة إلى اتخاذ أي إجراء من جانب MPOS.

### <a name="renew-a-self-signed-certificate"></a>تجديد شهادة موقعة ذاتيًا

لا تستخدم عينة الشهادة المتاحة في Retail SDK للإنتاج. يمكن استخدامها لأغراض التطوير فقط. لا يمكن تجديد عينة شهادة Contoso وستنتهي صلاحية عينة الشهادة المضمنة في الإصدار 10.0.16 من Retail SDK أو إصدار أقدم في 31 ديسمبر 2020. إذا تم استخدام هذه الشهادة، أو شهادة موقعة ذاتيًا، للتوقيع على Modern POS مخصصة، فهناك احتمال قوي بأن لا تعمل Modern POS بشكل صحيح بعد هذا التاريخ.
 
### <a name="impact"></a>التأثير
 
إذا كان ما ورد أعلاه صحيحاً، فستكون المشكلة التي ستواجهها عدم قدرة المثبت على العمل بعد 31 ديسمبر 2020. بحسب سياسات تكنولوجيا المعلومات للشركة المستخدمة، قد لا تتمكن Modern POS من العمل. من المهم أن تختبر ذلك عن طريق تغيير التاريخ مؤقتًا إلى تاريخ مستقبلي، لتحديد التأثير على مؤسستك.
 
### <a name="steps-to-determine-the-issue"></a>الخطوات المطلوبة لتحديد المشكلة
 
1.  استخدم إعدادات Windows لتغيير ساعة الكمبيوتر إلى تاريخ ووقت في السنه 2021.
2.  تحقق من إمكانية فتح Modern POS، ومن إمكانية حدوث تسجيل الدخول، ويمكن إكمال حركة.
3.  تحقق من إمكانية تشغيل مثبتة الخدمة الذاتية لـ Modern POS، وإذا كان الأمر كذلك، فسيتم التثبيت بنجاح.
4.  أعد إعدادات ساعة Windows إلى التاريخ والوقت الصحيحين.
 
إذا كان بإمكانك إكمال كل هذه الخطوات دون مشاكل، فستتمكن من العمل على الشهادة الحالية بعد 31 ديسمبر 2020.  
 
### <a name="steps-going-forward"></a>الخطوات من الآن فصاعدًا 

من المستحسن أن تقوم بتجديد الشهادة التي تم استخدامها في وقت سابق. نوصي بشدة بالحصول على شهادة جديده. للقيام بذلك، يجب تنفيذ أحد الإجراءات التالية:
 
- **مفضل** - الحصول على شهادة توقيع التعليمات البرمجية‬ من مرج مصدق موثوق.

- **غير مفضل** - إنشاء شهادة توقيع التعليمات البرمجية ذاتية التوقيع لاستخدامها. يستخدم هذا عادةً فقط لأغراض التطوير داخل مجال ولا يوصى به للإنتاج. 

- **متوفر كحل مؤقت** - استخدم شهادة Contoso المجددة لتوقيع التعليمات البرمجية. ويستخدم هذا عادة لأغراض الاختبار، لذلك من المستحسن نشره في الإنتاج.
 
بعد ذلك، قم بإنشاء حزمة Modern POS مخصصة جديدة موقعة باستخدام هذه الشهادة التي تم الحصول عليها من أحد الإجراءات المذكورة أعلاه. بحسب الشهادة، يجب اتباع إحدى الخطوات التالية:
 
- إذا كنت تستخدم شهادة جديدة وموثوقة (أو شهادة موقعة ذاتيًا جديدة)، فستتم مطالبتك بتثبيت شهادة جديدة على كل جهاز. بعد ذلك، تحتاج إلى استخدام حزمة Modern POS Package (المثبت) التي تم إنشاؤها حديثًا، وإلغاء تثبيت التطبيق الحالي، ثم إعادة تثبيت حزمة Modern POS الجديدة. ستحتاج إلى تنفيذ عملية تنشيط الجهاز لـ Modern POS على كل جهاز.

- في حالة استخدام شهادة Contoso التي تم تجديدها، ستتم مطالبتك بتثبيت الشهادة الجديدة على كل جهاز وتثبيت حزمة Modern POS (المثبت). لست مطالبًا بإلغاء التثبيت، ولكن يجب إعادة التثبيت على الجهاز. لا حاجة إلى تنشيط جهاز Modern POS. هذا الخيار هو حل مؤقت. استخدم هذا الخيار فقط لتجنب إعادة التنشيط وحل المشكلة قبل الحصول على شهادة جديدة موثوق بها.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
