---
title: "إعداد بيئات محلية ونشرها"
description: "يوفر هذا الموضوع معلومات حول كيفية تخطيط بيئة محلية وإعدادها ونشرها."
author: sarvanisathish
manager: AnnBe
ms.date: 08/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Unified Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: ar-sa
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>إعداد بيئات محلية ونشرها

يصف هذا المستند كيفية تخطيط عملية النشر وإعداد البنية الأساسية ونشر Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (في الموقع المحلي).

## <a name="finance-and-operations-components"></a>مكونات Finance and Operations

يتكون تطبيق Finance and Operations من ثلاث مكونات رئيسية:

- خادم كائنات التطبيق (AOS)
- المعلومات المهنية (BI)
- ‏‫إعداد التقارير المالية‬/‏‫أداة تقارير الإدارة‬

هذه المكونات تعتمد على برامج النظام التالية:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1، الذي يتضمن الميزات التالية:

    - تمكين فهرس البحث في النص الكامل.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > لن يتم تشغيل التطبيق إذا لم يتم تمكين البحث في النص الكامل.

- SQL Server Management Studio
- Standalone Microsoft Azure Service Fabric
- Windows PowerShell 5.0 أو إصدار أحدث
- خدمات الأمان المشترك لـ Active directory (AD FS) في نظام التشغيل Windows Server 2016

  يجب أن تكون وحدة التحكم بالمجال Windows Server 2012 R2 أو إصدار أحدث مع مستوى وظائفي للمجال من 2012 R2، أو أكبر

  لمزيد من المعلومات حول المستويات الوظيفية للمجال، راجع: 
  - [ما هي المستويات الوظيفية لـ Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [التعرف على المستويات الوظيفية لخدمات مجال Active Directory](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

يتم توزيع بت Finance and Operations عبر Microsoft Dynamics Lifecycle Services (LCS). قبل إجراء عملية النشر، يجب عليك شراء مفاتيح الترخيص من خلال قناة ["اتفاقية Enterprise"](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) وإعداد مشروع محلي في LCS. يمكن بدء عمليات النشر من خلال LCS فقط. للحصول على مزيد من المعلومات حول كيفية إعداد المشاريع المحلية في LCS، راجع [إنشاء مشروع محلي في Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>مصادقة

يعمل التطبيق المحلي مع AD FS. للتفاعل مع LCS، يجب أيضًا تكوين Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance and Operations يستخدم Standalone Service Fabric. للحصول على مزيد من المعلومات، راجع [وثائق Service Fabric](/azure/service-fabric/).

## <a name="infrastructure"></a>البنية الأساسية

تم تصميم Finance and Operations للعمل على بنية شديدة التقارب. يتضمن تكوين الأجهزة المكونات التالية:

- نظام مجموعة Standalone Service Fabric الذي يستند إلى الأجهزة الظاهرية لـ Windows Server 2016
- SQL Server (دعم Clustered SQL وAlways-On)
- AD FS للمصادقة
- مشاركة ملف التخزين الإصدار 3 من Server Message Block (SMB)
- اختياري: Microsoft Office Server 2017

للحصول على مزيد من المعلومات، راجع [متطلبات النظام](../get-started/system-requirements.md) وإرشادات ضبط الحجم.

### <a name="hardware-layout"></a>تخطيط الأجهزة

خطط للبيئة الأساسية ونظام مجموعة Service Fabric، استنادًا إلى ضبط الحجم الموصى به في [ضبط حجم الأجهزة للبيئات المحلية](../get-started/hardware-sizing-on-premises-environments.md). للحصول على مزيد من المعلومات حول كيفية تخطيط نظام مجموعة Service Fabric، راجع [تخطيط وإعداد عملية نشر نظام المجموعة المستقل Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

يعرض الجدول التالي مثالًا عن تخطيط الأجهزة. ويستخدم هذا المثال في هذا الموضوع لتوضيح عملية الإعداد.

> [!NOTE]
> يجب أن تتضمن العقدة الأساسية لنظام مجموعة Service Fabric ثلاث عقد على الأقل. في هذا المثال، تم تعيين **OrchestratorType** كنوع العقدة الأساسية.

| هدف الجهاز                                 | اسم الجهاز    | عنوان IP    |
|-------------------------------------------------|-----------------|---------------|
| وحدة التحكم بالمجال                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| خادم الملفات                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| نظام مجموعة SQL Always-On                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| العميل                                          | SQLAOCLIENT1    | 10.179.108.11 |
| نظام مجموعة Service Fabric/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| نظام مجموعة Service Fabric/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| نظام مجموعة Service Fabric/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| نظام مجموعة Service Fabric/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| نظام مجموعة Service Fabric/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| نظام مجموعة Service Fabric/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| نظام مجموعة Service Fabric/عقدة أداة تقارير الإدارة‬ | SQLAOSMR1       | 10.179.108.18 |
| نظام مجموعة Service Fabric/عقدة SSRS                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>الإعداد

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل بدء الإعداد، يجب استيفاء المتطلبات الأساسية التالية. إعداد هذه المتطلبات الأساسية خارج نطاق هذا المستند.

- تم تثبيت Active Directory Domain Services (AD DS) وتكوينها في شبكتك.
- تم نشر AD FS.
- تم تثبيت SQL Server وSSRS وManagement Studio.

### <a name="overview"></a>نظرة عامة

يجب إكمال الخطوات التالية لإعداد بنية Finance and Operations الأساسية.

1. تخطيط اسم المجال ومناطق DNS
2. تخطيط الشهادات والحصول عليها
3. تخطيط حسابات المستخدمين والخدمات
4. إنشاء مناطق DNS وإضافة سجلات A
5. ضم الأجهزة الظاهرية إلى المجال
6. إضافة البرامج المطلوبة إلى الأجهزة الظاهرية
7. تنزيل برامج الإعداد النصية من LCS
8. وصف تكوينك
9. تثبيت الشهادات
10. إعداد نظام مجموعة Service Fabric مستقل
11. تكوين اتصال LCS للمستأجر
12. إعداد مساحة تخزين الملفات
13. إعداد SQL Server
14. تكوين قواعد البيانات
15. تشفير بيانات الاعتماد
16. إعداد SSRS
17. تكوين AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>تخطيط اسم المجال ومناطق DNS

من المستحسن أن تستخدم اسم مجال تم تسجيله بشكل عام لعملية تثبيت إنتاج AOS. وبهذه الطريقة، يمكن الوصول إليه من خارج الشبكة، إذا كان الوصول من الخارج مطلوبًا.

على سبيل المثال، إذا كان مجال شركتك contoso.com، فقد تكون منطقتك لتطبيق Finance and Operations (محلي) d365ffo.onprem.contoso.com، وقد تكون أسماء الأجهزة المضيفة على الشكل التالي:

- ax.d365ffo.onprem.contoso.com للأجهزة AOS
- sf.d365ffo.onprem.contoso.com لنظام مجموعة Service Fabric

### <a name="plan-and-acquire-your-certificates"></a>تخطيط الشهادات والحصول عليها

تكون شهادات طبقة مآخذ التوصيل الآمنة (SSL)مطلوبة لتأمين نظام مجموعة Service Fabric وكافة التطبيقات التي يتم نشرها. بالنسبة إلى أحمال عمل الإنتاج ووضع الحماية، من المستحسن أن تحصل على الشهادات من مرجع مصدق (CA) مثل [DigiCert](https://www.digicert.com/ssl-certificate/) أو [Comodo](https://ssl.comodo.com/) أو [Symantec](https://www.websecurity.symantec.com/ssl-certificate) أو [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) أو [GlobalSign](https://www.globalsign.com/en/ssl/). إذا تم إعدادات مجالك بواسطة [خدمات شهادات Active Directory](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS)، فيمكنك إنشاء الشهادات عبر AD CS. يجب أن تحتوي كل شهادة على مفتاح خاص تم إنشاؤه لتبادل المفاتيح، ويجب أن يكون قابلاً للتصدير إلى ملف تبادل المعلومات الشخصية (pfx.).

يمكن استخدام الشهادات الموقعة ذاتيًا لأغراض الاختبار فقط. لتسهيل العمل، تشتمل البرامج النصية للإعداد على برامج نصية تعمل على إنشاء وتصدير الشهادات الموقعة ذاتيًا. كما ذكرنا، يجب استخدام هذه الشهادات لأغراض الاختبار فقط.

| الغرض                                      | الشرح | الاحتياجات الإضافية |
|----------------------------------------------|-------------|-------------------------|
| شهادة SQL Server SSL                   | تُستخدم هذه الشهادة لتشفير البيانات المرسلة عبر شبكة بين مثيل SQL Server وتطبيق عميل. | <p>يجب أن يتطابق اسم المجال الخاص بالشهادة على اسم المجال المؤهل بالكامل (FQDN) الخاص بمثيل SQL Server أو وحدة الإصغاء.</p><p>على سبيل المثال، إذا تمت استضافة وحدة الإصغاء SQL على الجهاز DAX7SQLAOSQLA، فسيكون اسم DNS للشهادة DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| شهادة Service Fabric Server            | تُستخدم هذه الشهادة للمساعدة في تأمين الاتصال من عقدة إلى عقدة بين عقد Service Fabric. تُستخدم هذه الشهادة أيضًأ كشهادة خادم يتم تقديمها إلى العميل الذي يتصل بنظام المجموعة. | <p>يجب أن يتطابق اسم المجال الخاص بالشهادة مع منطقة DNS حيث تتم استضافة AOS وService Fabric.</p><p>على سبيل المثال، قد يكون اسم المجال الخاص بالشهادة \*.onprem.contoso.com أو \*.contoso.com.</p><p>إذا كنت تستخدم شهادة أحرف بدل، فسيطبق حرف البدل على مستوى واحد فقط. يجب تطبيق مجال فرعي، اسم بديل للموضوع (SAN)، على الشهادة إذا كانت أكثر من مستوى واحد، مثل \*.contoso.com في المثال السابق.</p> |
| شهادة Service Fabric Client            | تُستخدم هذه الشهادة من قبل العملاء لعرض وإدارة نظام مجموعة Service Fabric. | |
| شهادة التشفير                     | يتم استخدام هذه الشهادة لتشفير معلومات حساسة مثل كلمة مرور SQL Server وكلمات مرور حسابات المستخدمين. | <p>يجب أن يتضمن استخدام مفتاح الشهادة تشفير البيانات (10) ويجب إلا يتضمن مصادقة الخادم أو مصادقة العميل.</p><p>للحصول على مزيد من المعلومات، راجع [إدارة البيانات السرية في تطبيقات Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| شهادة AOS SSL                          | <p>تُستخدم هذه الشهادة كشهادة خادم يتم تقديمها إلى عميل موقع ويب AOS. وتُستخدم أيضًا لتمكين شهادات بروتوكول Communication Foundation (WCF)/Simple Object Access.</p><p>يمكن استخدام شهادة Service Fabric Server هنا إذا كانت شهادة أحرف بدل.</p> | <p>يجب أن يتطابق اسم المجال الخاص بالشهادة مع منطقة DNS حيث تتم استضافة AOS وService Fabric.</p><p>على سبيل المثال، قد يكون اسم المجال الخاص بالشهادة \*.d365ffo.onprem.contoso.com أو \*.onprem.contoso.com أو \*.contoso.com.</p><p>إذا كنت تستخدم شهادة أحرف بدل، فسيطبق حرف البدل على مستوى واحد فقط. يجب تطبيق مجال فرعي، SAN، على الشهادة إذا كانت أكثر من مستوى واحد، مثل \*.contoso.com في المثال السابق.</p> |
| شهادة مصادقة جلسة العمل           | يتم استخدام هذه الشهادة من قبل AOS للمساعدة في تأمين معلومات جلسة عمل المستخدم. | وهي أيضًا شهادة **مشاركة الملفات** التي سيتم استخدامها عند إجراء عملية النشر من LCS. |
| شهادة تشفير البيانات والتوقيع على البيانات | يتم استخدام هذه الشهادات من قبل AOS لتشفير المعلومات الحساسة. | |
| شهادة عميل التقارير المالية       | تُستخدم هذه الشهادة للمساعدة في تأمين الاتصال بين خدمات التقارير المالية وAOS. | |
| شهادة التقارير                        | تُستخدم هذه الشهادة للمساعدة في تأمين الاتصال بين SSRS وAOS. | |
| شهادة وكيل محلي في الموقع المحلي           | <p>تُستخدم هذه الشهادة للمساعدة في تأمين الاتصال بين وكيل محلي مستضاف محليًا وLCS.</p><p>تعمل هذه الشهادة على تمكين العميل المحلي من العمل بالنيابة عن مستأجر Azure AD، ومن لاتصال بـ LCS لتنسيق عمليات النشر ومراقبتها.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>تخطيط حسابات المستخدمين والخدمات

يجب عليك إنشاء عدة حسابات للمستخدمين أو الخدمات لكي يعمل Finance and Operations (محلي). يجب عليك إنشاء مجموعة من حسابات الخدمات المدارة مجموعة (gMSAs) وحسابات المجال وحسابات SQL. يعرض الجدول التالي حسابات المستخدمين والغرض منها وأمثلة عن أسماء سيتم استخدامها في هذا الموضوع.

| حساب المستخدم                                            | النوع           | الغرض | اسم المستخدم |
|---------------------------------------------------------|----------------|---------|-----------|
| حساب خدمة تطبيق التقارير المالية         | gMSA           |         | Contoso\\svc-FRAS$ |
| حساب خدمة عملية التقارير المالية             | gMSA           |         | Contoso\\svc-FRPS$ |
| حساب خدمة مصمم النقرة الواحدة للتقارير المالية | gMSA           |         | Contoso\\svc-FRCO$ |
| حساب خدمة AOS                                     | gMSA           | يجب أن يتم إنشاء هذا المستخدم لكي يبقى صالحًا للمستقبل. نحن نخطط لتمكين AOS من العمل مع gMSA في الإصدارات القادمة. عند إنشاء هذا المستخدم أثناء الإعداد، سوف تساعد على ضمان إجراء عملية انتقال سلسة إلى gMSA. | Contoso\\svc-AXSF$ |
| حساب خدمة AOS                                     | حساب المجال | يستخدم AOS هذا المستخدم في إصدار GA. | Contoso\\AXServiceUser |
| مستخدم مسؤول DB SQL AOS                                   | مستخدم SQL       | يستخدم Finance and Operations هذا المستخدم للمصادقة مع SQL\*. سيتم أيضًا استبدال هذا المستخدم بمستخدم gMSA في الإصدارات القادمة. | AXDBAdmin |
| حساب خدمة وكيل النشر المحلي                  | gMSA           | يتم استخدام هذا الحساب بواسطة الوكيل المحلي لتنسيق عمليات النشر على عقد مختلفة. | Contoso\\Svc-LocalAgent$ |

\* تتم حماية اسم مستخدم SQL وكلمة المرور لمصادقة SQL، نظرًا لتشفيرهما وتخزينهما في مشاركة الملفات.

### <a name="create-dns-zones-and-add-a-records"></a>إنشاء مناطق DNS وإضافة سجلات A

يتكامل DNS مع AD DS، ويسمح لك بتنظيم الموارد في الشبكة وإدارتها والبحث عنها. أنشئ منطقة بحث أمامي في DNS وسجلات A لاسم مضيف AOS ونظام مجموعة Service Fabric. في مثال الإعداد هذا، اسم منطقة DNS هو d365ffo.onprem.contoso.com، وأسماء سجلات A/الأجهزة المضيفة هي كما يلي:

- **ax**.d365ffo.onprem.contoso.com لأجهزة AOS
- **sf**.d365ffo.onprem.contoso.com لنظام مجموعة Service Fabric

#### <a name="add-a-dns-zone"></a>إضافة منطقة DNS

استخدم الإجراء التالي لإضافة منطقة DNS.

1. سجل دخولك إلى جهاز وحدة التحكم بالمجال ، ثم انقر فوق **بدء**، وابدأ تشغيل إدارة DNS بكتابة **dnsmgmt.msc**.
2. انقر بزر الماوس الأيمن فوق اسم وحدة التحكم بالمجال، ثم انقر فوق **منطقة جديدة** \> **التالي**.
3. حدد **المنطقة الرئيسية**.
4. اترك خانة الاختيار **تخزين المنطقة في Active Directory (متوفرة فقط إذا كان خادم DNS في وحدة تحكم بالمجال قابلة للكتابة** محددة)، ثم انقر فوق **التالي**.
5. حدد **إلى جميع خوادم DNS قيد التشغيل على وحدات التحكم بالمجال في هذا المجال: Contoso.com**، ثم انقر فوق **التالي**.
6. حدد **منطقة البحث الأمامي**، ثم انقر فوق **التالي**.
7. أدخل اسم المنطقة الخاصة بإعدادك، ثم انقر فوق **التالي**. على سبيل المثال، أدخل **d365ffo.onprem.contoso.com**.
8. حدد **عدم السماح بالتحديثات الحيوية**، ثم انقر فوق **التالي**.

#### <a name="set-up-an-a-record-for-aos"></a>إعداد سجل A لـ AOS

في منطقة DNS الجديدة، قم بإنشاء سجل A واحد يسمى **ax.d365ffo.onprem.contoso.com** **لكل** عقدة نظام مجموعة Service Fabric من النوع **AOSNodeType**. لا تنشئ سجلات A لأنواع العقد الأخرى.

1. انقر بزر الماوس الأيمن فوق المنطقة الجديدة، ثم انقر فوق **مضيف جديد**.
2. أدخل اسم وعنوان IP الخاص بعقدة Service Fabric (على سبيل المثال، 10.179.108.12) ومن ثم انقر فوق **"إضافة مضيف"**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>إعداد سجل A للمنسق

في منطقة DNS الجديدة، قم بإنشاء سجل A يسمى **‎sf.d365ffo.onprem.contoso.com** **لكل** عقدة نظام مجموعة Service Fabric من النوع **‎OrchestratorType**. لا تنشئ سجلات A لأنواع العقد الأخرى.

1. انقر بزر الماوس الأيمن فوق المنطقة الجديدة، ثم انقر فوق **مضيف جديد**.
2. أدخل اسم وعنوان IP الخاص بعقدة Service Fabric (على سبيل المثال، 10.179.108.15) ومن ثم انقر فوق **"إضافة مضيف"**.

#### <a name="join-vms-to-the-domain"></a>ضم الأجهزة الظاهرية إلى المجال

يمكنك ضم كل واحد من الأجهزة الظاهرية إلى المجال عن طريق إكمال الخطوات المذكورة في [كيفية ضم Windows Server 2016 إلى مجال Active Directory](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). يمكنك أيضًا استخدام البرنامج النصي Windows PowerShell.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
بعد انضمام الأجهزة الظاهرية إلى المجال، أضف حسابات خدمات AOS (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) إلى مجموعة المسؤولين المحليين. يمكنك مراجعة المقالة [إضافة عضو إلى مجموعة محلية](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) لمعرفة كيفية القيام بذلك.

#### <a name="disable-user-access-control"></a>تعطيل التحكم في وصول المستخدم 

نفّذ البرنامج النصي التالي لتعطيل التحكم في وصول المستخدم" على **كل** عقدة Service Fabric.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> يجب إعادة تمهيد العقدة بعد انتهاء البرنامج النصي بنجاح.

#### <a name="add-prerequisite-software-to-vms"></a>إضافة البرامج المطلوبة إلى الأجهزة الظاهرية

يسرد الجدول التالي البرامج المطلوبة التي يجب تطبيقها على الأجهزة الخاصة بكل نوع عقدة.

> [!NOTE]
> يجب عليك إعادة تشغيل جهاز الكمبيوتر بعد تثبيت المكونات.

| نوع العقدة | المكون | أمر |
|-----------|-----------|---------|
| AOS       | برنامج تشغيل SNAC – ODBC | راجع [Microsoft ODBC Driver 13.1 لـ SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft.NET Framework الإصدار 2.0-3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft.NET Framework الإصدار 4.0-4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internet Information Services ‏(IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | حزم Microsoft Visual C++ القابلة لإعادة التوزيع لبرنامج Microsoft Visual Studio 2013 | راجع [حزم Microsoft Visual C++ القابلة لإعادة التوزيع لبرنامج Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | محرك قاعدة بيانات 2010 Microsoft Access القابل لإعادة التوزيع | راجع [محرك قاعدة بيانات 2010 Microsoft Access القابل لإعادة التوزيع](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework الإصدار 2.0-3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework الإصدار 4.0-4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 في الوضع **الأصلي** | |
| MR        | .NET Framework الإصدار 2.0-3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework الإصدار 4.0-4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | حزم Visual C++ القابلة لإعادة التوزيع لبرنامج Visual Studio 2013 | راجع [حزم Microsoft Visual C++ القابلة لإعادة التوزيع لبرنامج Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>تنزيل برامج الإعداد النصية من LCS

لقد قمنا بتوفير عدة برامج نصية للمساعدة في تحسين تجربة الإعداد. اتبع هذه الخطوات لتنزيل البرامج النصية للإعداد من LCS.

1. سجل دخولك إلى LCS (<https://lcs.dynamics.com/v2>).
2. في لوحة المعلومات، انقر فوق لوحة **مكتبة الأصول المشتركة**.
3. انقر فوق علامة تبويب **النموذج**.
4. في الشبكة، حدد الصف **Dynamics 365 for Operations - البرامج النصية للنشر المحلي**.
5. انقر فوق **الإصدارات**، وقم بتنزيل أحدث إصدار من البرامج النصية.

### <a name="describe-your-configuration"></a>وصف تكوينك

يوفر هذا القسم معلومات حول البرامج النصية التي يجب تشغيلها. وستتم مناقشة البرامج النصية بالترتيب الذي يجب أن تقوم بتشغيلها فيه. لتشغيل البرامج النصية، قم بملء ملف القالب في $(downloadPath)\\ConfigTemplate.xml. يصف ملف ConfigTemplate.xml أنظمة مجموعة Service Fabric والشهادات المستخدمة لتكوينها والحسابات التي يجب منحها حق الوصول إلى الشهادات ذات الصلة. في المثال الموضح، يتم ملء القيم لمثال البنية الأساسية التي ورد وصفها في هذا الموضوع. سيتم استخدام ملف القالب في القسم التالي.

#### <a name="create-the-domain-account-for-a-service-user"></a>إنشاء حساب المجال لمستخدم الخدمة

قم بتشغيل الأمر التالي لإنشاء حساب مستخدم المجال، contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>إنشاء gMSAs

1. قم بتغيير الدليل إلى **$(DownloadPath)**، وقم بتشغيل أمر Windows PowerShell التالي.

    > [!NOTE]
    > لا يقوم هذا البرنامج النصي بإنشاء المستخدمين. بدلاً من ذلك، يطبق الأوامر التي يجب تشغيلها يدويًا على جهاز وحدة التحكم بالمجال.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. قم بنسخ إخراج الأمر إلى نافذة Windows PowerShell. تأكد من إزالة فواصل الأسطر، وشغّل البنود في جهاز وحدة التحكم بمجال Active Directory باستخدام الامتيازات العالية المستوى (انقر بزر الماوس الأيمن، ثم انقر فوق **تشغيل كمسؤول**).
3. شغّل البرنامج النصي التالي على جهاز وحدة التحكم بمجال Active Directory للتأكد من إنشاء الحسابات بنجاح. احرص على تشغيل البرنامج النصي بعد قيامك باستبدال النمط الذي يتطابق مع مصطلحات التسمية لحسابات الخدمة.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. شغّل البرنامج النصي Export-AddGMSAsONVMScript.ps1 على جهاز العميل. يقوم هذا البرنامج النصي بإنشاء برامج نصية يتم تشغيلها على كل جهاز ظاهري لـ Service Fabric ويقوم بإضافتها إلى مجلد يتوافق مع كل اسم جهاز ظاهري.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>إيقاف IIS

استخدام بروتوكول سطح المكتب البعيد (RDP) لتوصيل كل جهاز ظاهري لـ Service Fabric، وأكمل خطوات الدليل في [بدء تشغيل خادم الويب أو إيقافه (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). بدلاً من ذلك، يمكنك استخدام برنامج Windows PowerShell النصي التالي باستخدام RDP للاتصال بكل جهاز ظاهري لـ Service Fabric.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_يجب أن يتم تثبيت ميزة IIS لكن تعطيلها إذ توجد بعض تبعيات المنتج._

### <a name="install-certificates"></a>تثبيت الشهادات

1. إذا حصلت على الشهادات التي تم سردها مسبقًا في هذا الموضوع من مرجع مصدق صالح، فاعمل على ملء اسم ملف pfx. وبصمة الإبهام للشهادات في الملف ConfigTemplate.xml. قم بتعيين السمة **generateSelfSignedCert** إلى **False** والسمة **exportable** إلى **False**. انسخ ملفات pfx. إلى المجلد $(DownloadPath)\\InfrastructureScripts\\Certs.
2. إذا كنت تستخدم الشهادات الموقعة ذاتيًا (لأغراض الاختبار فقط)، فقم بتشغيل البرنامج النصي التالي. لإنشاء شهادات موقعة ذاتيًا، في ملف ConfigTemplate.xml، تأكد من تعيين **generateSelfSignedCert‎** إلى **True** ومن تعيين **قابل للتصدير** إلى **True**. سيقوم البرنامج النصي بتحديث XML مع بصمة الإبهام للشهادات.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. قم بتصدير الشهادات الجديدة باستخدام المفتاح الخاص (ملف pfx.). استخدم البرنامج النصي التالي لإنشاء وتشغيل أوامر التصدير في Windows PowerShell. سيتم وضع ملفات pfx. في المجلد Certs.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > يجب أن تكون الشهادات مثبتة وموجودة في cert:\\CurrentUser\\My. يجب أن تكون الشهادات أيضًا قابلة للتصدير.

    إذا كنت تستخدم شهادات موقعة ذاتيًا، فانتقل إلى القسم التالي. لست بحاجة إلى إكمال هذا الإجراء.

4. بعد تصدير ملفات pfx. أو نسخها إلى مجلد $(DownloadPath)\\InfrastructureScripts\\Certs، قم بتشغيل الأوامر التالية لإنشاء البرامج النصية التي سيتم وضعها في المجلدات التي تتوافق مع الأجهزة الظاهرية.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. انسخ البرامج النصية في كل مجلد إلى الأجهزة الظاهرية التي تتوافق مع اسم المجلد.
6. في كل جهاز ظاهري، قم تشغيل البرامج النصية التالية حسب ترتيب ظهورها.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>إعداد نظام مجموعة Service Fabric مستقل

1. قم بتشغيل الأمر التالي لإنشاء ملف ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    للحصول على مزيد من المعلومات، راجع [الخطوة 1ب: إنشاء نظام مجموعة متعدد الأجهزة](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) و[حماية نظام مجموعة مستقل على Windows باستخدام شهادات X.509](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security)و[إنشاء نظام مجموعة مستقل يتم تشغيله على Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. قم بتنزيل [حزمة تثبيت Service Fabric المستقل](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) في إحدى عقد Service Fabric. بعد تنزيل ملف zip، يمكنك إلغاء حظره بالنقر بزر الماوس الأيمن فوق ملف zip ثم النقر فوق **خصائص**. في مربع الحوار، حدد خانة الاختيار **إلغاء الحظر** في الجزء السفلي الأيسر.
3. انسخ ملف zip إلى إحدى العقد في نظام مجموعة Service Fabric، ثم اعمل على فك ضغطه.
4. قم بتشغيل الأوامر التالية لإنشاء قاعدة جدار حماية واردة على المنفذي 443 و445 في كافة العقد.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. قم بتشغيل الأوامر التالية لإنشاء قاعدة جدار حماية واردة على المنفذ 80 لعقدة SSRS فقط.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. انسخ ملف ClusterConfig.json إلى الموقع التثبيت غير المضغوط لنظام مجموعة Service Fabric المستقل.
7. انتقل إلى موقع التثبيت غير المضغوط في Windows PowerShell باستخدام الامتيازات العالية، وشغّل الأمر التالي لاختبار ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. في حالة نجاح الاختبار، قم بتشغيل الأمر التالي لنشر نظام المجموعة.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. بعد إنشاء نظام المجموعة، افتح مستكشف Service Fabric على أي جهاز عميل للتحقق من صحة التثبيت:

    1. قم بتثبيت شهادة عميل Service Fabric في CurrentUser\\My إذا لم تكن مثبتة.
    2. انتقل إلى **إعدادات IE** \> **وضع التوافق**، وقم بإلغاء تحديد خانة الاختيار **عرض مواقع الإنترانت في وضع التوافق**.
    3. انتقل إلى `https://sf.d365ffo.onprem.contoso.com:19080`، حيث sf.d365ffo.onprem.contoso.com هو اسم المضيف لنظام مجموعة Service Fabric المحدد في المنطقة. إذا لم يتم تكوين تحليل اسم DNS، فاستخدم عنوان IP للجهاز.
    4. حدد شهادة العميل. تظهر صفحة **مستكشف Service Fabric**.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>تكوين اتصال LCS للمستأجر

يتم تنسيق نشر وخدمة Finance and Operations من خلال LCS باستخدام وكيل محلي للموقع المحلي. لتأسيس اتصال من LCS إلى مستأجر Finance and Operations، يجب تكوين شهادة تمكّن الوكيل المحلي من العمل بالنيابة عن مستأجر Azure AD (على سبيل المثال، Contoso.Onmicrosoft.com).

استخدم شهادة الوكيل المحلي التي حصلت عليه من مرجع مصدق أو الشهادة الموقعة ذاتيًا التي تم إنشاؤها باستخدام البرامج النصية.

وحدها حسابات المستخدمين التي لديها دور دليل المسؤول العمومي يمكنها إضافة شهادات لتخويل LCS. بشكل افتراضي، سيكون الشخص الذي يسجل للحصول على Microsoft Office 365 لمؤسستك بمؤسستك المسؤول العمومي للدليل.

> [!NOTE]
> يجب عليك تكوين الشهادة مرة واحدة تمامًا لكل مستأجر. باستطاعة جميع البيئات المحلية استخدام نفس الشهادة للاتصال بـ LCS.

1. قم بتنزيل وتثبيت أحدث إصدار من Azure PowerShell على جهاز عميل. للحصول على مزيد من المعلومات، راجع [تثبيت وتكوين Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. سجّل الدخول إلى [مدخل Azure الخاص بالعميل](https://portal.azure.com) للتحقق من أن لديك دور دليل المسؤول العمومي.
3. قم بتشغيل البرنامج النصي التالي من $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>إعداد مساحة تخزين الملفات

يجب إعداد مشاركتين من مشاركات ملفات SMB 3.0 عالية التوفر. لمزيد من المعلومات حول كيفية تمكين SMB 3.0، راجع[تحسينات أمان SMB](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
يتعذر على تفاوض اللهجة الآمن الكشف عن حالات العودة إلى الإصدار السابق من SMB 2.0 أو 3.0 إلى SMB 1.0 أو منعها. ولهذا السبب، وللاستفادة من الإمكانيات الكاملة لتشفير SMB، نوصي بشدة بتعطيل خادم SMB 1.0

> [!NOTE]
> للمساعدة في ضمان حماية بياناتك أثناء استقرارها في بيئتك، يجب تمكين تشفير محرك BitLocker على كل جهاز. لمزيد من المعلومات حول كيفية تمكين BitLocker، راجع [BitLocker: كيفية النشر على Windows Server 2012 والاصدارات الأحدث](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- مشاركة الملفات التي تقوم بتخزين مستندات المستخدم التي يتم تحميلها إلى AOS (على سبيل المثال، \\\\DAX7SQLAOFILE1\\aos-storage).
- مشاركة الملفات التي تقوم بتخزين آخر ملفات الإصدار والتكوين لتنسيق عملية النشر (على سبيل المثال، \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > احرص على إبقاء مسار مشاركة الملفات هذه قصيرًا قدر المستطاع لتجنب تجاوز الحد الأقصى لطول المسار على الملفات التي سيتم وضعها في المشاركة.

1. على جهاز مشاركة الملفات، قم بتشغيل الأمر التالي.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>إعداد مشاركة ملفات \\\\DAX7SQLAOFILE1\\aos-storage

2. في إدارة الخادم، حدد **خدمات الملفات والتخزين** \> **مشاركات**.
3. انقر فوق **المهام** \> **مشاركة جديدة** لإنشاء مشاركة جديدة باسم **aos-storage**.
4. امنح أذونات **التعديل** لكل جهاز في نظام مجموعة Service Fabric ما عدا **OrchestratorNodeType‎**.
5. امنح أذونات **التعديل** لمستخدم مجال AOS (contoso\\AXServiceUser) ومستخدم gMSA (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>إعداد مشاركة ملفات وكيل \\\\DAX7SQLAOFILE1\\

6. عد إلى إدارة الخادم، وحدد **خدمات الملفات والتخزين** \> **مشاركات**.
7. انقر فوق **المهام** \> **مشاركة جديدة** لإنشاء مشاركة جديدة باسم **agent**.
8. امنح أذونات **التحكم الكامل** لمستخدم gMSA لوكيل النشر المحلي agent (contoso\\svc-LocalAgent$).

### <a name="set-up-sql-server"></a>إعداد SQL Server

1. قم بتثبيت SQL Server 2016 SP1 مع التوفر العالي، إما كأنظمة مجموعات SQL التي تحتوي على شبكة منطقة التخزين (SAN) أو في تكوين Always-On.  تأكد من تثبيت **محرك قاعدة البيانات وخدمات إعداد التقارير والبحث عن كامل النص**و**أدوات الإدارة**.
> [!NOTE]
> الرجاء التأكد من إعداد SQL Always On وفقًا لـ [تحديد صفحة مزامنة البيانات الأولية (معالجات مجموعات Always On Availability)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) واتبع [لإعداد قواعد البيانات الثانوية يدويًا](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. قم بتشغيل خدمة SQL كمستخدم مجال.
3. احصل على شهادة SSL من مرجع مصدق لتكوين Finance and Operations. لأغراض تتعلق بالاختبار، يمكنك إنشاء شهادة موقعة ذاتيًا واستخدامها.

**الشهادة الموقعة ذاتيًا لمثيل Clustered SQL**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**الشهادة الموقعة ذاتيًا لمثيل Always-On SQL**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. باستخدام الشهادة، أكمل الخطوات الواردة في [كيفية تمكين تشفير SSL لمثيل SQL Server باستخدام Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) لتكوين SSL على خادم SQL.‬
5. لكل عقدة في نظام المجموعة، اتبع هذه الخطوات. تأكد من إجراء التغييرات على العقدة غير النشطة وتجاوز الفشل بعد إجراء التغييرات.

    1. استورد الشهادة إلى LocalMachine\\My.
    2. امنح أذونات الشهادات إلى حساب الخدمة الذي يتم استخدامه لتشغيل خدمة SQL. في Microsoft Management Console (MMC)، انقر بزر الماوس الأيمن فوق الشهادة (certlm.msc)، ومن ثم انقر فوق **المهام** \> **إدارة المفاتيح الخاصة**.
    3. أضف بصمة إبهام الشهادة إلى HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. في Microsoft SQL Server Configuration Manager، قم بتعيين **ForceEncryption** إلى **Yes**.

6. قم بتصدير المفتاح العمومي للشهادة (ملف cer.)، ثم قم بتثبيته في الجذر الموثوق لكل عقدة Service Fabric.

### <a name="configure-the-orchestratordata-database"></a>تكوين قاعدة بيانات OrchestratorData

1.  أنشئ قاعدة بيانات فارغة، وقم بتسميتها **OrchestratorData**. يتم استخدام قاعدة البيانات هذه بواسطة الوكيل المحلي في الموقع المحلي لتنسيق عمليات النشر.
2.  امنح الوكيل المحلي أذونات gMSA (svc-LocalAgent$) **db\_owner** على قاعدة البيانات:

    1. في الشجرة، قم بتوسيع اسم الخادم، قم بتوسيع **الأمان** \> **عمليات تسجيل الدخول**، ثم انقر بزر الماوس الأيمن وانقر فوق **تسجيل دخول جديد**.

        ![أمر تسجيل دخول جديد](./media/OPSetup_01_NewLogin.png)


    2. ابحث عن حساب الخدمة **svc-LocalAgent$**. انقر فوق **المواقع**، وحدد **الدليل بأكمله**، ثم انقر فوق **أنواع الكائن**، وحدد **حساب الخدمة**.

        ![مربع حوار تحديد المستخدم أو حساب خدمة أو المجموعة](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. قم بتعيين **Assign ServerRole** إلى **Public**.
    4. قم بتعيين إذن دور قاعدة البيانات **db\_owner** إلى قاعدة بيانات OrchestratorData.

### <a name="configure-the-finance-and-operations-database"></a>تكوين قاعدة بيانات Finance and Operations

1. سجل دخولك إلى LCS (<https://lcs.dynamics.com/v2>).
2. في لوحة المعلومات، انقر فوق لوحة **مكتبة الأصول المشتركة**.
3. انقر فوق علامة تبويب **النموذج** 
4. في الشبكة، انقر فوق **Dynamics 365 for Operations on-premises, Enterprise edition - بيانات العرض التوضيحي** لتنزيل ملف zip.
5. يحتوي ملف zip على ملفات فارغة وملفات bak. للعرض التوضيحي. استنادًا إلى احتياجاتك، اختر ملف bak. الملائم. على سبيل المثال، إذا كنت تحتاج إلى بيانات العرض التوضيحي، فيمكنك استعادة الملف AxBootstrapDB_Demodata.bak. 
6. استعد قاعدة البيانات AxBootstrapDB_DemoData.bak.
7. أعد تسمية قاعدة البيانات **AXDBRAIN**.
8. شغّل الاستعلامات التالية في قاعدة البيانات التي تمت استعادتها.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. قم بتحديث ملفات قاعدة البيانات:

    1. انقر بزر الماوس الأيمن فوق قاعدة البيانات، ثم انقر فوق **خصائص**.
    2. انقر فوق **ملفات** لتغيير خصائص ملف قاعدة البيانات.
    3. في الحقل **الحجم الأولى (ميغابايت)**، أدخل قيمة أكبر من 5,120.

        ![مربع حوار خصائص قاعدة البيانات](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. بالنسبة إلى **AXDBBuild\_Data**، عيّن الحقل **نمو تلقائي/تكبير** إلى **200** ميغابايت.
    5. بالنسبة إلى **AXDBBuild\_Log**، عيّن الحقل **Autogrowth/Maximize** إلى **500** ميغابايت.

        ![مربع حوار تغيير النمو التلقائي](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. قم بإنشاء مستخدم جديد تم تمكين مصادقة SQL له (axdbadmin).
6. استخدم المعلومات الموجودة في الجدول التالي لتعيين أدوار المستخدمين وقاعدة البيانات.

    | المستخدم             | النوع    | دور قاعدة البيانات |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. امنح مستخدم svc-AXSF$ ومستخدم axdbadmin SQL حق الوصول إلى الأدوار التالية في قاعدة بيانات tempdb:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. في Management Studio، قم بتشغيل أوامر Transact SQL (T-SQL) التالية:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. قم بتشغيل الأمر التالي:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>تكوين قاعدة بيانات التقارير المالية

1.  أنشئ قاعدة بيانات فارغة، وقم بتسميتها **FinancialReporting**.
2.  استخدم المعلومات الموجودة في الجدول التالي لتعيين أدوار المستخدمين وقاعدة البيانات.

    | المستخدم             | النوع | دور قاعدة البيانات |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>تشفير بيانات الاعتماد

1. على أي جهاز عميل، قم بتثبيت شهادة التشفير في LocalMachine\\My certificate store.
2. امنح المستخدم الحالي حق الوصول للقراءة إلى المفتاح الخاص لهذه الشهادة.
3. أنشئ ملف Credentials.json كما هو موضح هنا.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** هي كلمة مرور مستخدم المجال المشفرة لمستخدم مجال AOS domain user (contoso\\axserviceuser).
    - **SqlUser** هو مستخدم SQL المشفر (axdbadmin) الذي لديه حق الوصول إلى قاعدة بيانات Finance and Operations (AXDBRAIN) و**SqlPassword** هي كلمة مرور SQL المشفرة.

4. انسخ ملف json. إلى مشاركة ملفات SMB، \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. قم بتحديث الملف Credentials.json بالقيم المشفرة.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. في Credentials.json، استبدل **\<encryptedDomainUserPassword\>** بكلمة مرور المجال المشفرة.
    2. استبدل **\<encryptedSqlUser\>** بمستخدم Finance and Operations SQL المشفر.
    3. استبدل **\<encryptedSqlPassword\>** بكلمة مرور Finance and Operations SQL.
    
### <a name="set-up-ssrs"></a>إعداد SSRS

1.  قبل أن تبدأ، تأكد من تثبيت المتطلبات الأساسية المدرجة في بداية هذا الموضوع.
2.  اتبع الخطوات من أجل [تكوين خدمات SQL Server Reporting Services للنشر المحلي](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>تكوين AD FS

قبل أن تتمكن من إكمال هذا الإجراء، يجب أن يتم نشر AD FS على Windows Server 2016. لمزيد من المعلومات حول كيفية نشر AD FS، راجع [دليل نشر Windows Server 2016 و2012 R2 AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

يتطلب Finance and Operations تكوينًا إضافيًا يتجاوز تكوين AD FS الجاهز الافتراضي. للخطوات التالية، يتم تشغيل Windows PowerShell على جهاز تم تثبيت خدمة دور AD FS عليه. يجب أن تتوفر لحساب المستخدم الأذونات الكافية لإدارة AD FS. على سبيل المثال، يجب أن يتوفر للمستخدم حساب مسؤول مجال.

1. قم تكوين معرف AD FS بحيث يتطابق مع مُصدر ‏‫الرمز المميز AD FS.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. يجب عليك تعطيل المصادقة المتكاملة لنظام Windows (WIA) لاتصالات مصادقة الإنترانت إلا إذا قمت بتكوين AD FS للبيئات المختلطة. للحصول على مزيد من المعلومات حول كيفية تكوين WIA بحيث يمكن استخدامها مع AD FS، راجع [تكوين المستعرضات لاستخدام مصادقة Windows المتكاملة (WIA) مع AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. لتسجيل الدخول، يجب أن يكون عنوان البريد الإلكتروني للمستخدم عبارة عن إدخال مصادقة مقبولة.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

لكي تثق خدمة AD FS بتطبيق Finance and Operations لتبادل للمصادقة، يجب تسجيل إدخالات تطبيقات مختلفة في AD FS ضمن مجموعة تطبيقات AD FS. لتسريع عملية الإعداد والمساعدة في تقليل الأخطاء، يمكنك استخدام البرنامج النصي التالي للتسجيل. انسخ البرنامج النصي Publish-ADFSApplicationGroup.ps1 ودليل D365FO-OP إلى جهاز تم فيه تثبيت خدمة دور AD FS. بعد ذلك، قم بتشغيل البرنامج النصي باستخدام حساب مستخدم، مثل حساب المسؤول، يملك أذونات كافية لإدارة AD FS. لمزيد من المعلومات حول كيفية استخدام البرنامج النصي، راجع الوثائق المدرجة في البرنامج النصي. دوّن ملاحظة حول معرفات العميل المحددة في الإخراج، إذ ستتم مطالبتك بهذه المعلومات في LCS في خطوة لاحقة.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

يجب أن تكون وحدة تحكم إدارة AD FS مماثلة للشكل التوضيحي التالي. لفتح إدارة الخادم، انقر فوق **أدوات** \> **إدارة AD FS**، ثم في أسفل طريقة عرض الشجرة إلى اليمين، انقر فوق **مجموعات التطبيقات**. انقر نقرًا مزدوجًا فوق مجموعة التطبيقات لعرض مزيد من التفاصيل.

![خصائص مجموعة التطبيقات](./media/OPSetup_05_ApplicatioGroupProperties.png)

أخيرًا، لإجراء فحص للسلامة، تأكيد أنه باستطاعة الوصول إلى عنوان URL لتكوين AD FS OpenID Configuration على عقدة Service Fabric من النوع **AOSNodeType** عند طريق الانتقال إلى `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` في مستعرض الويب. إذا تلقيت رسالة تشير إلى أن الموقع غير آمن، فهذا يعني عدم بإضافة شهادة AD FS SSL إلى مخزن الشهادات الجذر الموثوقة. يتم وصف هذه الخطوة في دليل نشر AD FS. إذا وصلت بنجاح إلى عنوان URL، فسيتم إرجاع ملف JavaScript Object Notation (JSON) يحتوي على تكوين AD FS، وسترى أن عنوان URL لـ AD FS هو عنوان موثوق.

مع هذه الخطوة، سيكتمك إعداد البنية الأساسية. تصف المقاطع التالية كيفية الانتقال إلى [LCS](https://lcs.dynamics.com) لإعداد الموصل ونشر بيئة Dynamics 365 for Finance and Operations.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>تكوين الموصل وتثبيت وكيل محلي للموقع المحلي

1. سجل دخولك إلى [LCS](https://lcs.dynamics.com/) وافتح مشروع التطبيق المحلي.
2. في قائمة الهامبرجر، انقر فوق **إعدادات المشروع**.

    ![الأمر "إعدادات المشروع"](./media/OPSetup_06_ProjectSettings.png)

3. انقر فوق **موصلات محلية**.
4. انقر فوق **إضافة** لإنشاء موصل جديد.
5. على علامة تبويب **إعداد البنية الأساسية للمضيف** ، قم بتنزيل مثبت الوكيل.

    ![الزر "تنزيل مثبت الوكيل" على علامة تبويب "إعداد البنية الأساسية للمضيف"](./media/OPSetup_07_DownloadAgentInstaller.png)

6. تأكد من أن ملف zip غير محظور. انقر بزر الماوس الأيمن فوق الملف، ثم انقر فوق **خصائص**، ثم حدد **إلغاء الحظر**.
7. قم بفك ضغط مثبت الوكيل على إحدى عقد Service fabric من النوع **OrchestratorType**.
8. على علامة تبويب **تكوين الوكيل**، أدخل إعدادات التكوين.
9. احفظ التكوين ومن ثم انقر فوق **تنزيل التكوينات** لتنزيل ملف تكوين localagent-config.json.

    ![الزر "تنزيل التكوينات" على علامة تبويب "تكوين الوكيل"](./media/OPSetup_08_DownloadConfigurations.png)

10. انسخ ملف localagent-config.json إلى الجهاز حيث توجد حزمة مثبت الوكيل.
11. في نافذة موجه الأوامر، قم بتشغيل الأمر التالي عن طريق الانتقال إلى المجلد الذي يحتوي على مثبت الوكيل.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > يجب أن يكون لدى المستخدم الذي يقوم بتشغيل هذا الأمر أذونات **db\_owner** على قاعدة بيانات OrchestratorData.
    
12. بمجرد أن يتم تثبيت الوكيل المحلي بنجاح، انتقل مرة أخرى إلى الموصل المحلي في LCS.
13. على علامة التبويب **التحقق من صحة الإعداد**، انقر فوق الزر **إرسال رسالة إلى الوكيل**. سيؤدي ذلك إلى اختبار اتصال LCS بالوكيل المحلي. عندما يتم تأسيس الاتصال بنجاح، سوف تبدو الصفحة مماثلة للرسم أدناه.

     ![التحقق من صحة الوكيل](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>نشر بيئة Dynamics 365 for Finance and Operations (محلي)

1. انتقل إلى المشروع المحلي في LCS، انتقل إلى **البيئة**، **وضع الحماية** وانقر فوق **تكوين**
2. حدد **طبولوجيا البيئة** وانتقل عبر المعالج لبدء عملية النشر.
3. سوف يلتقط الوكيل المحلي طلب النشر، ويطلق عملية النشر ويتواصل مع LCS عندما يصبح جاهزًا.

