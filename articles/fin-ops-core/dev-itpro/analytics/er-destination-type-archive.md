---
title: نوع وجهة إعداد التقارير الإلكترونية للأرشيف
description: يوفر هذا الموضوع معلومات حول كيفيه تكوين وجهه أرشفه لكل مجلد أو مكون ملف لتنسيق التقارير الكترونيه (ER).
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a9e0f07241de003dd2971e0d336f89795ad1319b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348010"
---
# <a name="archive-er-destination-type"></a>نوع وجهة إعداد التقارير الإلكترونية للأرشيف

[!include [banner](../includes/banner.md)]

يمكنك تكوين وجهة أرشيف لكل مكون **مجلد** أو **ملف** لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة. واستنادًا إلى إعداد الوجهة، يتم تخزين المستند المنشأ كمرفق لسجل قائمة مهام إعداد التقارير الإلكترونية. لعرض النتائج، انتقل إلى **إدارة مؤسسة** \> **التقارير الإلكترونية** \> **وظائف إعداد التقارير الإلكترونية**.

يمكنك استخدام هذا الخيار لإرسال المستند المنشأ إلى مجلد Microsoft SharePoint أو مساحة تخزين Microsoft Azure. عيّن الخيار **ممكّن** إلى **نعم** لإرسال المخرجات إلى وجهة تم تعريفها بواسطة نوع المستند المحدد. أنواع المستندات المتوفرة للتحديد هي فقط تلك التي تم تعيين المجموعة فيها إلى **ملف**. يمكنك تحديد [أنواع](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) المستندات في **إدارة المؤسسة** \> **إدارة المستند** \> **أنواع المستندات**. يُعد تكوين وجهات التقارير الإلكتروني التكوين نفسه لنظام إدارة المستندات.

[![صفحة أنواع المستندات.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

يحدد الموقع المكان حيث تم حفظ الملف. بعد تمكين وجهة **الأرشيف**، يمكن حفظ النتائج تنفيذ التكوين في أرشيف الوظيفة. يمكنك عرض النتائج في **إدارة مؤسسة** \> **التقارير الإلكترونية** \> **الوظائف المؤرشفة لإعداد التقارير الإلكترونية**.

> [!NOTE]
> حدد نوع مستند لأرشيف الوظيفة بالتنقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية** \> **معلمات التقارير الإلكترونية**. للحصول على مزيد من التفاصيل، راجع [تكوين إطار عمل إعداد التقارير الإلكترونية (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

يمكنك حفظ ملف في مجلد معين في SharePoint. لتحديد خادم SharePoint الافتراضي، انتقل إلى **إدارة المؤسسة** \> **إدارة المستندات** \> **معلمات إدارة المستندات**. في علامة التبويب **SharePoint**، كوِّن مجلد SharePoint. يمكنك بعد ذلك تحديده كمجلد حفظ مخرجات التقارير الإلكترونية. يجب تحديد موقع **SharePoint** في نوع المستند هذا.

[![تحديد مجلد SharePoint.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

عند تعيين موقع نوع المستند إلى **مساحة تخزين Azure**، يمكنك حفظ ملف في مساحة تخزين Azure.

> [!NOTE] 
> يقوم إطار عمل إعداد التقارير الإلكترونية بتخزين الملفات بشكل دائم في تخزين Azure Blob بخلاف إطار عمل إدارة البيانات الذي يطبق نهج الاحتفاظ لمدة سبعة أيام للمستندات التي يجب معالجتها. لمزيد من المعلومات، راجع [واجهة برمجة التطبيقات للحصول على حالة الرسالة](../data-entities/recurring-integrations.md#api-for-getting-message-status) و[واجهة برمجة تطبيقات التحقق من الحالة](../data-entities/data-management-api.md#status-check-api). سيتم تخزين الملفات المتعلقة بالتقارير الإلكترونية في تخزين Azure Blob كمرفقات في سجلات جدول التطبيق طالما كان ذلك ضروريًا. سيتم حذف ملف واحد من تخزين Azure Blob مع سجل جدول التطبيق الذي تم إرفاق هذا الملف به.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)
- [وجهات إعداد التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md)
- [تكوين إدارة المستندات](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]