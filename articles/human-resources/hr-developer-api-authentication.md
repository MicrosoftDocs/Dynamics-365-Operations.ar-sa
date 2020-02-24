---
title: المصادقة
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008008"
---
# <a name="authentication"></a>المصادقة

يقدم هذا المقال معلومات عامة حول كيفية المصادقة مع واجهة برمجة تطبيقات بيانات Microsoft Dynamics 365 Human Resources.

## <a name="overview"></a>نظرة عامة

تعد واجهة برمجة تطبيقات البيانات للموارد البشرية بمثابة تطبيق OData. لمزيد من المعلومات، راجع [‬‏‫بروتوكول البيانات المفتوحة (OData)‬](../fin-ops-core/dev-itpro/data-entities/odata.md).

يجب أن يقوم التطبيق الخاص بك بالمصادقة كمتصل مخوّل قبل أن تتعامل واجهة API مع الطلبات التي تتلقاها من التطبيق الخاص بك.

## <a name="fundamentals"></a>القواعد الأساسية

لاستدعاء API للبيانات، يجب أن يحصل التطبيق الخاص بك على رمز مميز للوصول من النظام الأساسي لهويه Microsoft. يحتوي الرمز المميز للوصول على معلومات حول التطبيق الخاص بك والإذن الذي يجب عليه استدعاء الموارد في الموارد البشرية.

### <a name="access-token"></a>الرمز المميز للوصول

الرموز المميزة للوصول التي يصدرها النظام الأساسي لهويه Microsoft هي رموز JavaScript Object Notation (JSON) مميزة للويب (JWTs) يتم ترميزها باستخدام base64. وهي تحتوي على معلومات (مطالبات) تستخدمها واجهة API للبيانات (وواجهات API الويب الأخرى التي تم تأمينها بواسطة النظام الأساسي لهويه Microsoft) للتحقق من المتصل والتأكد من أنه يملك الأذونات الصحيحة لتنفيذ العملية التي يطلبها. أثناء المكالمات، يمكنك التعامل مع رموز الوصول المميزة على أنها غير شفافة. يجب عليك دائمًا نقل رموز الوصول المميزة عبر قناة آمنة ، مثل أمان طبقة النقل (TLS) وبروتوكول نقل النص التشعبي الآمن (HTTPS).

وفيما يلي مثال لرمز وصول مميز تم إصداره بواسطة النظام الأساسي لهويه Microsoft.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

لطب واجهة API للبيانات، قم بإرفاق الرمز المميز للوصول كرمز حامل لرأس التخويل في طلب HTTP الخاص بك. فيما يلي مثال على ذلك.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>تسجيل استمارة جديدة باستخدام مدخل Azure

1. قم بتسجيل الدخول إلى [مدخل Microsoft Azure ](https://portal.azure.com) باستخدام حساب العمل أو المؤسسة التعليمية، أو حساب Microsoft شخصي.

2. إذا كان الحساب الخاص بك يمنحك حق الوصول إلى أكثر من مستأجر، فحدد حسابك في الركن الأيمن العلوي، وعيّن جلسة المدخل الخاصة بك على مستأجر Azure Active Directory (Azure AD) الذي تريده.

3. في الجزء الأيمن ، حدد خدمة **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق \> تسجيل جديد**.

4. عندما تظهر صفحة **تسجيل تطبيق**، أدخل معلومات تسجيل التطبيق الخاص بك:

    - **الاسم**: أدخل اسم التطبيق ذي معني الذي سيظهر لمستخدمي التطبيق.
    - **أنواع الحسابات المعتمدة**: حدد أنواع الحسابات التي يجب أن يدعمها تطبيقك.

        | أنواع الحسابات المعتمدة | ‏‏الوصف |
        |-------------------------|-------------|
        | الحسابات الموجودة في الدليل التنظيمي هذا فقط | حدد هذا الخيار إذا كنت تقوم بتصميم تطبيق خاص بالأعمال التجارية. لا يتوفر هذا الخيار الا إذا قمت بتسجيل التطبيق في دليل.<p>يتم تعيين هذا الخيار إلى **Azure AD مستأجر واحد فقط**.</p><p>ويعد هذا الخيار هو الخيار الافتراضي الا إذا كنت تقوم بتسجيل التطبيق خارج أحد الدلائل. وفي هذه الحالة، يكون الخيار الافتراضي هو **Azure AD حسابات Microsoft شخصية ومتعددة المستأجرين**.</p> |
        | الحسابات الموجودة في أي دليل تنظيمي | حدد هذا الخيار لاستهداف كافة العملاء التجاريين والتعليميين.<p>يتم تعيين هذا الخيار إلى **Azure AD مستأجرين متعددين فقط**.</p><p>إذا كنت قد قمت بتسجيل التطبيق كـ **Azure AD مستأجر واحد فقط** يمكنك استخدام ريشة **‏‫المصادقة‬**، لتحديثها إلى **Azure AD مستأجرين متعددين فقط** ثم الرجوع إلى **Azure AD مستأجر واحد فقط**.</p> |
        | الحسابات الموجودة في أي دليل تنظيمي وحسابات Microsoft الشخصية | حدد هذا الخيار لاستهداف أكبر مجموعة من العملاء.<p>يتم تعيين هذا الخيار إلى **Azure AD حسابات Microsoft شخصية ومتعددة المستأجرين**.</p><p>إذا كنت قد قمت بتسجيل التطبيق كـ **Azure AD حسابات Microsoft شخصية ومتعددة المستأجرين** فلن تتمكن من تغيير هذا الإعداد في واجهة المستخدم (UI). بدلاً من ذلك، يجب عليك استخدام محرر بيان التطبيق لتغيير أنواع الحسابات المدعومة.</p> |

    - **عنوان URI لإعادة التوجيه (اختياري)** - حدد نوع التطبيق الذي تقوم بتصميمه: **ويب** أو **عميل عام (هاتف محمول وسطح المكتب)**. ثم أدخل عنوان URI لإعادة التوجيه (أو عنوان URL الخاص بالرد) للتطبيق.

        - بالنسبة لتطبيقات الويب، قم بتوفير عنوان URL الأساسي الخاص بالتطبيق. على سبيل المثال، قد يكون `http://localhost:31544` هو عنوان URL الخاص بتطبيق ويب الذي يتم تشغيله علي الجهاز المحلي الخاص بك. ثم يقوم المستخدمون باستخدام عنوان URL هذا لتسجيل الدخول إلى تطبيق عميل ويب.
        - بالنسبة لتطبيقات العميل العامة، قم بتوفير عنوان URL الذي يستخدمه Azure AD لإرجاع استجابات الرمز المميزة. أدخل قيمة خاصة بالتطبيق، مثل `myapp://auth`.

        لمشاهدة أمثلة معينة لتطبيقات الويب أو التطبيقات الأصلية، راجع قوالب التشغيل السريع في [النظام الأساسي للهوية Microsoft (الذي كان يسمى سابقًا Azure Active Directory للمطورين)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. ضمن **أذونات API**، حدد **إضافة إذن**. ثم، في علامة التبويب **واجهات API التي تستخدمها مؤسستي** ابحث عن **Dynamics 365 Human Resources** وأضف الإذن **user\_impersonation** إلى التطبيق الخاص بك. معرف التطبيق للموارد البشرية هو f9be0c49-aa22-4ec6-911a-c5da515226ff. استخدم هذا المعرف للتأكد من أنك قمت باختيار التطبيق الصحيح.

6. حدد **السجل**.

   [![تسجيل تطبيق جديد في مدخل Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

يقوم Azure AD بتعيين معرف تطبيق فريد (معرف العميل) إلى التطبيق الخاص بك، ثم ينقلك إلى صفحة **نظرة عامة** للتطبيق الخاص بك. لإضافة المزيد من الإمكانات إلى التطبيق، يمكنك تحديد خيارات التكوين الأخرى، مثل الخيارات الخاصة بالعلامة التجارية والشهادات والأسرار.

## <a name="retrieving-an-access-token"></a>استرداد الرمز المميز للوصول

ستعتمد المواصفات الخاصة بكيفية استرداد رمز مميز للوصول للاتصال بواجهة API لبيانات الموارد البشرية على التقنيات التي تستخدمها لتطوير تطبيق العميل. على سبيل المثال، قد [تقوم بالاختبار باستخدام أداة مساعدة لجهة خارجية](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (مثل Postman) أو تطوير تطبيق وحده تحكم C# أو خدمة ويب أو إنشاء عميل javascript/TypeScript.

مثال لتطبيق عميل C#:
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

بمجرد استرداد رمز وصول مميز، ستقوم بتمرير الرمز المميز في رأس التخويل كرمز مميز لحامل مع كل طلب تقوم بإرساله إلى واجهة API للبيانات، كما هو موضح أعلاه.
