---
title: إنشاء محرك إدارة نقل جديد
description: يوضح هذا الموضوع كيفيه إنشاء محرك أداره نقل جديد في Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678111"
---
# <a name="create-a-new-transportation-management-engine"></a>إنشاء محرك إدارة نقل جديد

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفيه إنشاء محرك أداره نقل جديد في Dynamics 365 Supply Chain Management. 

تقوم محركات إدارة النقل (TMS) بتعريف المنطق المستخدم لإنشاء ومعالجه معدلات النقل في إدارة النقل. توفر Supply Chain Management عده أنواع مختلفه من المشغلات التي تقوم بحساب معلمات مختلفه ، مثل الأسعار وأوقات الانتقال وعدد المناطق التي سيتم تقاطعها اثناء النقل. يوضح هذا المقال كيفيه استخدام بيئة تطوير Visual Studio Microsoft مع أدوات تطوير Supply Chain Management لإنشاء ونشر مشغل TMS جديد ومن ثم كيفيه اعداد المشغل في عمليات لمزيد من المعلومات حول المحركات ، راجع [محركات أداره النقل](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>إنشاء محرك TMS جديد

يوضح هذا القسم كيفيه إنشاء مكتبه فئة لها تطبيق TMS ، وكيفيه الرجوع اليها من نموذج Supply Chain Management.

1. لنشر المشغلات الجديدة ، يجب ان يكون لديك طراز سيحتوي علي المحركات. في القائمة **Dynamics 365**&gt;**أداره النماذج** ، انقر فوق **إنشاء نموذج** لإنشاء نموذج جديد. في الصفحة الاولي من معالج **إنشاء نموذج** ، قم بتسميه النموذج **TMSEngines**. 

   [![إنشاء نموذج](./media/012.png)](./media/012.png)

2. في الصفحة التالية ، حدد **إنشاء حزمه جديده**. 

   [![إنشاء حزمة جديدة](./media/021.png)](./media/021.png)

3. في الصفحة التالية ، حدد نموذج **ApplicationSuite** المراد الرجوع اليه. (النموذج **ApplicationPlatform** محدد مسبقًا.) 

   [![تحديد النموذج المراد الرجوع اليه.](./media/032.png)](./media/032.png)

4. في الصفحة التالية ، انقر فوق **إنهاء** لتاكيد إنشاء نموذج جديد. 

   [![إكمال إنشاء النموذج.](./media/042.png)](./media/042.png)

5. في حل جديد ، قم بإنشاء مشروع Supply Chain Management جديد ، وقم بتسميته **TMSThirdParty**. في خصائص المشروع ، قم بتعيين نموذج المشروع إلى **TMSEngines**.
6. أضافه مكتبه فئة C\# جديده إلى الحل الخاص بك وقم بتسميتها **ThirdPartyTMSEngines**.
7. في المشروع ThirdPartyTMSEngines، أضف مراجع للتجميعات الخاصة بـ Supply Chain Management:
   -   تجميعات التطبيقات التي تمكنت الرجوع إلى أنواع X++. يمكن العثور علي هذه التجميعات في المواقع التالية. \[جذر الحزم\] هو مسار الموقع الذي يتم فيه وضع كافة التجميعات المنشورة ، مثل C:\\الحزم.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   تجميعات اطار العمل التي تمكن الوصول إلى البيانات وLINQ والوظائف المساعدة. يمكن العثور علي كافة هذه التجميعات في الحاوية \[جذر الحزم\]\\.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   التجميع الأساسي TMS (الذي يحتوي علي المشغلات) والتجميع الأساسي TMS (والذي يحتوي علي مساعدين وثوابت وتعريفات فئات نقل البيانات وغيرها). يمكن العثور علي هذه التجميعات في المواقع التالية.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. أعاده تسميه الفئة C\# التي يتم إنشاؤها تلقائيا في المشروع ThirdPartyTMSEngines إلى **SampleRatingEngine**.
9. تنفيذ المحرك. ونظرا لأننا نقوم بإنشاء محرك السعر في هذا المثال ، فاننا نجمع من الفئة الاساسيه لمحركات التقييم. وتقوم الفئة الاساسيه بتنفيذ معظم واجهه محرك المعدل (**TMSFwkIRateEngine**). نحتاج فقط لتنفيذ أسلوب السعر. للاحتفاظ بهذا المثال بسيط ، سنقوم بجعل هذا الأسلوب يسجل معدل السرعة الثابتة 100. يمكنك إنشاء المحركات التي تقوم بتطبيق اي من واجهات المحرك ، مثل **TMSFwkIAccessorialEngine**. ويتم تعريف كافة واجهات المحرك بالكامل في X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. قم ببناء الحل.
11. أضف مرجعا جديدا إلى المشروع TMSThirdParty. يجب ان يشير المرجع إلى مشروع ThirdPartyTMSEngines. عند الانتهاء ، يجب ان يبدو الحل الخاص بك بهذا الشكل. 

    [![الحل الذي يتضمن مرجعا لمشروع TMSThirdParty.](./media/052.png)](./media/052.png)

12. قم ببناء الحل. تحقق من ان المكتبة الجديدة تظهر في عقده **المراجع** في مستكشف التطبيق. 

    [![المكتبة الجديدة في عقده مراجع مستكشف التطبيق.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>توزيع المشغل TMS كحزمه

والطريقة الوحيدة لنشر مشغلات TMS الجهات الخارجية من خلال أحدي حزم النشر. يوصي باستخدام هذه الطريقة في بيئة التشغيل. في بيئة التطوير ، يمكنك نسخ التجميعات يدويا ، كما هو موضح في القسم التالي ، "اعداد محرك TMS في Supply Chain Management". لنشر المحرك كحزمة، اتبع الخطوات التالية:

1. في القائمة **Dynamics 365**&gt;**نشر** ، انقر فوق <strong>إنشاء حزمه توزيع</strong>.
2. في مربع الحوار **إنشاء حزمه نشر** ، حدد نموذج TMSEngines، وادخل المسار حيث تريد تخزين ملفات الحزمة الخاصة بك. 

   [![تحديد نموذج TMSEngines.](./media/071.png)](./media/071.png)

3. يمكنك الآن نشر الحزمة إلى بيئة الهدف. لبرنامج تعليمي ، راجع [تثبيت حزمه قابله للنشر](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>إعداد محرك TMS في Supply Chain Management

يوضح هذا القسم كيفيه اعداد Supply Chain Management لاستخدام TMS engine ، كما يوضح كيفيه استخدام المحرك الجديد الذي قمنا بإنشاءه بسعر التسوق. يستخدم المثال في هذا القسم شركة بيانات العرض التوضيحي USMF.

1. قم بإنشاء مشغل جديد كما هو موضح في القسم "إنشاء محرك TMS جديد".
2. قم ببناء حلك.
3. قم بنسخ التجميع الناتج إلى الموقع الثنائي لخادم Supply Chain Management، وفي حاوية \[AOSWebRoot\]. **ملاحظه:** تكون هذه الخطوة ذات صله فقط في بيئة التطوير. في بيئة التشغيل، يجب النشر من خلال حزمه نشر. للحصول علي الإرشادات ، راجع القسم السابق ، "نشر محرك TMS كحزمه."
4. في Supply Chain Management، في الصفحة **محركات المعدلات** ، قم بإنشاء محرك معدلات جديد. يجب ان يشير المحرك إلى تجميع المحركات الذي تم إنشاؤه عن طريق إنشاء مكتبه فئة المحرك وفئة المحرك التي قمت بتطبيقها. 

   [![إنشاء محرك تصنيف جديد في الصفحة المعدل الخاص بالمحركات.](./media/081.png)](./media/081.png)

5. قم بإنشاء شركه شحن تستخدم محرك معدل العينات. وبما ان المحرك لا يستخدم إيه بيانات ، فلن تحتاج إلى تعيين المعدل الرئيسي. 

   [![إنشاء شركة شحن جديدة.](./media/092.png)](./media/092.png)

6. في الصفحة **منضدة عمل مسار التصنيف**، انقر فوق **تصنيف المتجر**. يجب ان تري تصنيف 100.00 من SampleCarrier، كما هو موضح في لقطه الشاشة التالية. في هذا المثال ، نقوم بتصنيف التسوق من المستودع 24 إلى العميل US-004. ومع ذلك ، وبسبب ان المعدل بترميز ثابت ، ستشاهد دائما معدل 100.00.

   [![منضدة عمل مسار التصنيف](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>تلميحات ونصائح

- إذا كنت تستخدم أدوات تطوير Supply Chain Management، فمن المفيد أضافه مشروع جديد إلى الحل الخاص بك. إذا قمت بتعيين هذا المشروع كمشروع بدء التشغيل وقامت ببدء جلسة تصحيح ، يمكنك تصحيح كل من التعليمات البرمجية X++ وC\# في نفس جلسة تصحيح الأخطاء.
- كل مره تقوم فيها بتغيير وأعاده التحويل البرمجي لمشروع ThirdPartyTMSEngines الخاص بك ، يجب عليك نسخ التجميع الناتج يدويا إلى الموقع الثنائي أو النشر عبر حزمه نشر. والا ، يمكنك التشغيل باستخدام تجميع تالف.
- بعد تنفيذ العمليات الخاصة بـ TMS في Supply Chain Management، قد تقوم العملية التابعة لعامل خدمات معلومات الإنترنت (IIS) بتامين التجميع ThirdPartyTMSEngines بحيث لا يمكن تحديث التجميع. في هذه الحالة ، قم باعاده تشغيل عمليه w3svc.

### <a name="whitepaper"></a>مستند تقني

لمزيد من المعلومات، قم بتنزيل الصفحة البيضاء التالية (المكتوبة لدعم AX2012، ولكن لا يزال يتم تطبيقها لـ Dynamics 365 Supply Chain Management)

- [تنفيذ محركات أداره النقل ونشرها](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]