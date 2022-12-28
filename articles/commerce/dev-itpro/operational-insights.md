---
title: إعداد Operational Insights
description: يوضح هذا المقال كيفية إعداد واستخدام ميزة Operational Insights في Microsoft Dynamics 365 Commerce.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832111"
---
# <a name="set-up-operational-insights"></a>إعداد Operational Insights

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفية إعداد واستخدام ميزة Operational Insights في Microsoft Dynamics 365 Commerce.

يُعد Operational Insights ميزة Dynamics 365 Commerce المصممة لإعطار العملاء رؤية أفضل في حالة الخدمة ووظائف الأعمال عن طريق إرسال بيانات تتبع الاستخدام مباشرة إلى عميل يملك حساب Application Insights.

من خلال تمكين Operational Insights في البيئات الخاصة بك في Commerce headquarters، يمكنك جمع قائمة بالأحداث من Commerce Scale Unit (CSU) وأجهزة نقطة البيع (POS) الخاصة بك. ويمكن أن تساعد هذه الأحداث على فهم أفضل كيفية لتنفيذ الأنظمة الخاصة بك، وتتيح لك مراقبة المعايير التقنية والأعمال الأساسية.

وحتى في حالة عدم الرغبة في تجميع بيانات تتبع الاستخدام هذه طوال الوقت، فيمكنك الاستفادة بسرعة في تمكين أو تعطيل المجموعة للبيئات المحددة. وبهذه الطريقة، يمكن أن تساعدك بيانات تتبع الاستخدام في استكشاف الأخطاء وإصلاحها أو التصحيح أثناء التطوير أو في الإنتاج.

## <a name="access-logs-in-application-insights"></a>تسجيل الوصول في Application Insights

للوصول إلى سجلات أحداث التشخيص لمكونات Commerce CSU ونقاط POS عبر Application Insights، أكمل الإجراءات الواردة في هذا القسم.

### <a name="minimum-version-requirements-for-csu"></a>الحد الأدنى لمتطلبات الإصدار لـ CSU

تحتوي CSU على الحد الأدنى التالي من متطلبات الإصدار:

- 10.0.23 (إصدار خادم البيع بالتجزئة 9.33.22062.15 وإصدارات لاحقة)
- 10.0.24 (إصدار خادم البيع بالتجزئة 9.34.22062.14 وإصدارات لاحقة)
- 10.0.25 (إصدار خادم البيع بالتجزئة 9.35.22062.13 وإصدارات لاحقة)
- 10.0.26 والإصدارات اللاحقة (جميع الإصدارات)

### <a name="enable-diagnostic-events-in-application-insights"></a>تمكين الأحداث التشخيصية في Application Insights

> [!IMPORTANT]
> إذا كنت قد استخدمت إصدار معاينة من Operational Insights مستقبلاً، فإنه يجب عليك استخدام الإجراء التالي لتمكين Operational Insights. بهذه الطريقة، فإنك تضمن من أنه يمكن متابعة الوصول الأمن والموثوق به إلى الأحداث.

لتمكين أحداث تشخيص مكون Commerce، يجب أن يكون لديك حساب Application Insights. يمكنك استخدام حساب موجود أو [إنشاء حساب جديد](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). لأسباب تتعلق بخصوصية البيانات، نُوصي باستخدام حسابات Application Insights منفصلة للإنتاج وبيئة الاختيار وبيانات التطوير. بعد إنشاء حساب، يجب تمكين ميزة **Operational Insights** في المركز الرئيسي.

لتمكين الأحداث في Application Insights، اتبع هذه الخطوات.

1. في المركز الرئيسي، افتح مساحة عمل **إدارة الميزات** وتمكين الميزة **Operational Insights**.
1. انتقل إلى **إدارة النظام \> الإعداد \> Operational Insights**.
1. في علامة التبويب **تكوين**، قم بتعيين الخيار **أحداث قناة Commerce** إلى **نعم**.
1. في علامة التبويب **البيئات**، أدخل قيم **معرف بيئة LCS‬** و **وضع البيئة** لكل بيئة حيث تخطط لاستخدام Application Insights. يمكنك العثور على معرف بيئة كل بيئة في الصفحة **تفاصيل البيئة** لتلك البيئة في Microsoft Dynamics Lifecycle Services. هذه الخطوة مطلوبة للمساعدة في منع إرسال أحداث التشخيص بدون قصد إلى بيئة غير صحيحة عند تنفيذ عمليات نسخ قاعدة البيانات.
1. في علامة التبويب **Application Insights التسجيل**، حدد قيمة Application Insights **مفتاح الأدوات** وقيمة **وضع البيئة** المقابلة للبيئات التي تخطط استخدام كل حساب Application Insights بها.
1. بعد إكمال التكوين السابق، يجب تشغيل الوظيفة **وظيفة CDX رقم 1110** . يمكنك انتظار تشغيل هذه الوظيفة بالجدول الخاص بها، أو يمكنك تشغيلها يدويًا.
1. في Lifecycle Services، انتقل إلى **تفاصيل البيئة \> Commerce \> إدارة**، حدد مثيل CSU، ثم حدد **إعادة التشغيل**. كرر تلك الخطوة لكل CSU.
1. كرر الخطوات السابقة لكل بيئة تحدد استخدام Application Insights بها.

> [!NOTE]
> - تخضع أحداث بيانات تتبع الاستخدام الموجودة في Operational Insights للتغيير. ونُوصي باستخدام أحداث Operational Insights لإجراء التحليل المبدئي واستكشاف الأخطاء وإصلاحها بنفسك، وليس لتعريف لوحات المعلومات أو التنبيهات. في حالة استخدام أحداث لأغراض تتجاوز استكشاف أخطاء الخدمة الذاتية وإصلاحها، نُوصي بالتحقق من صحة الاستعلامات وتحديثها بعد كل إصدار من إصدارات CSU/POS.
> - واعتبارًا من Commerce الإصدار 10.0.29، فإن الإجراءات الواردة في هذا القسم تتيح أيضًا إمكانية دفق أحداث Operational Insights الخاصة بنقطة البيع إلى حساب Application Insights الخاص بك. لمزيد من المعلومات، راجع [Operational Insights لنقطة البيع - الأحداث والاستعلامات](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>استخدام الملف DLLHost.exe.config للتحكم في أحداث Operational Insights لنقطة البيع

لاستخدام الملف DLLHost.exe.config للتحكم في أحداث Operational Insights لنقطة البيع، اتبع الإجراءات التالية.

1. في محرر النص، افتح الملف **DLLHost.exe.config** على **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. في القسم **diagnosticsSection**، أزل اسم الفئة **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**.
1. احفظ الملف.

### <a name="disable-diagnostic-events-in-application-insights"></a>تعطيل الأحداث التشخيصية في Application Insights

> [!IMPORTANT]
> إذا كنت ترغب في تعطيل أحداث التشخيص ولم تعد ترسلها إلى  Application Insights، فإنه يجب إكمال الإجراء التالي. لا يمكنك تعطيل الميزة في إدارة الميزات فقط.

لتعطيل الأحداث في Application Insights، اتبع هذه الخطوات.

1. في المركز الرئيسي، انتقل إلى **إدارة النظام \> Operational Insights**.
1. في علامة التبويب **تكوين**، قم بتعيين الخيار **أحداث قناة Commerce** إلى **لا**.
1. بعد إكمال التكوين السابق، يجب تشغيل الوظيفة **وظيفة CDX رقم 1110** . يمكنك انتظار تشغيل هذه الوظيفة بالجدول الخاص بها، أو يمكنك تشغيل الوظيفة يدويًا.
1. في Lifecycle Services، انتقل إلى **تفاصيل البيئة \> Commerce \> إدارة**، حدد مثيل CSU، ثم حدد **إعادة التشغيل**. كرر تلك الخطوة لكل CSU.
1. كرر الخطوات السابقة لكل بيئة تحدد إيقاف تشغيل Application Insights بها.

لتعطيل الأحداث التشخيصية لبيئة واحدة، احذف مفتاح الأدوات في علامة التبويب **تسجيل Application Insights** في الصفحة **Operational Insights**. ثم أكمل الخطوتين 3 و 4 من الإجراء السابق.

> [!NOTE]
> في Commerce الإصدار 10.0.29 وما بعده، فإن الخطوات الواردة في هذا القسم تُعيق أيضًا إمكانية دفق أحداث Operational Insights الخاصة بنقطة POS إلى حساب Application Insights الخاص بك. 
