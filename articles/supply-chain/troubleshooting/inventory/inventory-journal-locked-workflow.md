---
title: تم تأمين دفتر يومية المخزون ولا تعمل وظيفة مجموعة سير العمل
description: تم تأمين أحد دفاتر يومية المخزون من خلال عملية أخرى ولم يتم إصدارها
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475445"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>تم تأمين دفتر يومية المخزون ولا تعمل وظيفة مجموعة سير العمل

## <a name="symptoms"></a>العلامات

تم تامين أحد دفاتر يوميه المخزون من خلال عمليه أخرى ولم يتم إصدارها. علي سبيل المثال، في حاله حدوث خطا غير معروف اثناء الترحيل (الذي يعد عمليه تامين النظام)، فقد يظل دفتر اليومية في حاله تامين النظام. في هذه الحالة، سيقوم معالج عنصر عمل سير العمل بطرح خطا اثناء تامين التحقق من الصحة.

## <a name="resolution"></a>الحل

قم بتسجيل الدخول إلى مثيل SQL Server لـ Supply Chain Management، وتحقق ما إذا كان قد تم تعيين **InventJournalTable.SystemBlocked** إلى *1*. وإذا كان الأمر كذلك، فتاكد من ان الدفتر لا يجب ان يكون في حاله تامين، ثم قم باعاده تعيين **InventJournalTable.SystemBlocked** إلى القيمة *0*.
