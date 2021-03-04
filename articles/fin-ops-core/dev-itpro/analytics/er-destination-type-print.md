---
title: نوع وجهة إعداد التقارير الإلكترونية للطابعة
description: يوضح هذا الموضوع كيفية تكوين وجهة طابعة لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة بتنسيق PDF أو تنسيق Microsoft Office (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: b7a279dcb30e7681ae654ab17d898a5364391d57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679596"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>وجهة الطابعة

[!include [banner](../includes/banner.md)]

يمكنك إرسال مستند مُنشأ مباشرة إلى طابعة الشبكة للطباعة المباشرة.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل البدء، يجب تثبيت وكيل توجيه المستند وتكوينه، ثم تسجيل طابعات الشبكة. لمزيد من المعلومات، راجع [تثبيت وكيل توجيه المستند لتمكين طباعة الشبكة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)

## <a name="make-the-printer-destination-available"></a>توفير وجهة الطابعة

لتوفير وجهة **الطابعة** في مثيل Microsoft Dynamics 365 Finance الحالي، انتقل إلى مساحة عمل **إدارة الميزات**، وشغَّل الميزات التالية بالترتيب التالي:

1. تحويل المستندات الصادرة للتقارير الإلكترونية من تنسيقات Microsoft Office إلى PDF
2. عامل توجيه المستندات كوجهة إعداد التقارير الإلكترونية للمستندات الصادرة

[![تشغيل ميزة وجهة طابعة إعداد التقارير الإلكترونية في إدارة الميزات](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>إمكانية التطبيق

لا يمكن تكوين وجهة **الطابعة** إلا لمكونات الملف المستخدمة لإنشاء مخرجات في تنسيق pdf القابل للطباعة (عناصر تنسيق ملف PDF أو دمج PDF) أو تنسيق Microsoft Office Excel/Word (ملف Excel). عند إنشاء مخرجات بتنسيق PDF، يتم إرسالها إلى طابعة. عند إنشاء المخرجات بتنسيق Microsoft Office، يتم تحويلها تلقائيًا إلى تنسيق PDF ثم إرسالها إلى طابعة.

### <a name="limitations"></a>قيود

هذه الميزة هي ميزة معاينة وهي خاضعة لشروط الاستخدام الموضحة في [شروط الاستخدام الإضافية لمعاينات المستخدمة لمعاينات Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).

لا يتم تطبيق وجهة **الطابعة** إلا لعمليات نشر المجموعة فقط.

### <a name="use-the-printer-destination"></a>استخدام وجهة الطابعة

1. عيِّن الخيار **ممكَّن** على **نعم** لإرسال مستند منشأ إلى طابعة.
2. في الحقل **اسم الطابعة**، حدد طابعة الشبكة المطلوبة.
3. عيِّن الخيار **هل تريد الحفظ في أرشيف الطباعة؟** على **نعم** لتخزين المخرجات المنشأة في أرشيف الطباعة، بحيث يكون متوفرًا لمزيد من عمليات الطباعة. للوصول إلى المخرجات المؤرشفة لاحقًا، انتقل إلى **إدارة المؤسسة**\>**‏‫الاستعلامات والتقارير‬**\>**أرشيف التقارير**.

[![استخدام وجهة الطابعة](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> لا يلزم تشغيل خيار **لتحويل إلى PDF‬** عند تكوين وجهة **الطابعة**. سيتم التحويل إلى PDF لأغراض الطباعة حتى في حالة إيقاف تشغيل الخيار.

لاستخدام [اتجاه صفحة](electronic-reporting-destinations.md#SelectPdfPageOrientation) محدد عند طباعة مستند صادر في تنسيق Excel، يجب تشغيل خيار **التحويل إلى PDF**. عندما تقوم بتعيين خيار **التحويل إلى PDF** إلى **نعم**، يصبح حقل **اتجاه الصفحة** متاحًا. في حقل **اتجاه الصفحة**، يمكنك تحديد اتجاه الصفحة.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)
- [وجهات إعداد التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]