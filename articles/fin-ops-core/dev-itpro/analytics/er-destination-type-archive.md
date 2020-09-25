---
title: نوع وجهة إعداد التقارير الإلكترونية للأرشيف
description: يوفر هذا الموضوع معلومات حول كيفية تكوين وجهة أرشيف لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745575"
---
# <a name="archive-destination"></a>وجهة الأرشيف

[!include [banner](../includes/banner.md)]

يمكنك تكوين وجهة أرشيف لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة. واستنادًا إلى إعداد الوجهة، يتم تخزين المستند المنشأ كمرفق لسجل قائمة مهام إعداد التقارير الإلكترونية.

يمكنك استخدام هذا الخيار لإرسال المستند المنشأ إلى مجلد Microsoft SharePoint أو مساحة تخزين Microsoft Azure. عيّن الخيار **ممكّن** إلى **نعم**لإرسال المخرجات إلى وجهة تم تعريفها بواسطة نوع المستند المحدد. أنواع المستندات المتوفرة للتحديد هي فقط تلك التي تم تعيين المجموعة فيها إلى **ملف**. يمكنك تحديد [أنواع](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) المستندات في **إدارة المؤسسة** \> **إدارة المستند** \> **أنواع المستندات**. يُعد تكوين وجهات التقارير الإلكتروني التكوين نفسه لنظام إدارة المستندات.

[![صفحة أنواع المستندات](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

يحدد الموقع المكان حيث تم حفظ الملف. بعد تمكين وجهة **الأرشيف**، يمكن حفظ النتائج تنفيذ التكوين في أرشيف الوظيفة. يمكنك عرض النتائج في **إدارة مؤسسة** \> **التقارير الإلكترونية** \> **الوظائف المؤرشفة لإعداد التقارير الإلكترونية**.

> [!NOTE]
> حدد نوع مستند لأرشيف الوظيفة بالتنقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية** \> **معلمات التقارير الإلكترونية**. للحصول على مزيد من التفاصيل، [تكوين إطار عمل إعداد التقارير الإلكترونية (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

يمكنك حفظ ملف في مجلد معين في SharePoint. لتحديد خادم SharePoint الافتراضي، انتقل إلى **إدارة المؤسسة** \> **إدارة المستندات** \> **معلمات إدارة المستندات**. في علامة التبويب **SharePoint**، كوِّن مجلد SharePoint. يمكنك بعد ذلك تحديده كمجلد حفظ مخرجات التقارير الإلكترونية. يجب تحديد موقع **SharePoint** في نوع المستند هذا.

[![تحديد مجلد SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

عند تعيين موقع نوع المستند إلى **مساحة تخزين Azure**، يمكنك حفظ ملف في مساحة تخزين Azure.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)
- [وجهات إعداد التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md)
- [تكوين إدارة المستندات](../../fin-ops/organization-administration/configure-document-management.md)
