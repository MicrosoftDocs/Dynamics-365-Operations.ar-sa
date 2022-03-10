---
title: تقييم جميع الإجراءات لتوجيهات مواقع وحدة SKU المتعددة
description: تمت إضافة ميزة جديدة لتقييم كافة الإجراءات لتوجيهات مواقع SKU المتعددة. ترشدك هذه الصفحة إلى المعلومات حول كيفية تشغيلها.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102953"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>لا يقوم الخيار المتعدد SKU بتقييم العديد من إجراءات التوجيه للموقع

## <a name="symptoms"></a>العلامات

لا يقوم موجه المواقع الخاصة بنوع أمر عمل *أوامر المبيعات* ونوع العمل *تخزين* بتقييم الإجراءات الموجهة متعددة المواقع عند تحديد الخيار **SKU متعددة**. يتم تقييم الاجراء الخاص بالتوجيه في الموقع الأول فقط.

## <a name="resolution"></a>الحل

تمت أضافه ميزه جديده، *تقييم كافة الإجراءات لتوجيهات المواقع SKU المتعددة*، في الإصدار 10.0.15 (راجع [قاعدة المعارف 4579866 ](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). هذه الميزة تقيم كافة الإجراءات لموجهات مواقع SKU متعددة. اعتبارًا من الإصدار 10.0.21 من Supply Chain Management، يتم تشغيل هذه الميزة افتراضيًا.  هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها، اعتبارًا من Supply Chain Management 10.0.25. بإمكان المسؤولين استخدام صفحة [إدارة الميزات](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتمكينها أو تعطيلها إذا لزم الأمر.
