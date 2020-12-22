---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء
description: يوضح هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر العديد من الفواتير وأوامر العملاء في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458353"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء

[!include [banner](includes/banner.md)]


يصف هذا المقال وظيفتين لتحسين عمليات إرجاع أوامر العملاء عبر عدة فواتير. 

## <a name="enable-refunds-over-multiple-captures"></a>تمكين المبالغ المستردة عبر عمليات الالتقاط المتعددة

تُمكن هذه الميزة العديد من المبالغ المستردة المرتبطة لنفس أمر العميل. 

1. انتقل إلى مساحة عمل **إدارة الميزات** وابحث عن **‏‫تمكين المبالغ المستردة عبر عمليات الالتقاط المتعددة‬**.
2. حدد **‏‫تمكين المبالغ المستردة عبر عمليات الالتقاط المتعددة‬** ثم انقر **تمكين**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>تمكين الحساب المناسب للضريبة للمرتجعات التي تحتوي على كمية جزئية

تضمن هذه الوظيفة مساواة الضرائب في النهاية لمبلغ الضريبة المحصل بالأصل وذلك عند إرجاع أمر باستخدام فواتير متعددة. 

1. انتقل إلى مساحة عمل **إدارة الميزات** وابحث عن **‏‫‏‫تمكين الحساب المناسب للضريبة للمرتجعات التي تحتوي على كمية جزئية‬**.
2. حدد **تمكين الحساب المناسب للضريبة للمرتجعات التي تحتوي على كمية جزئية** ثم انقر **تمكين**. 


## <a name="process-returns"></a>معالجة المرتجعات

بعد تشغيل هذه الوظائف ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.

عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر. بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها. سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.

في حالة إرجاع الأمر بالكامل، يكون مبلغ الضرائب المرتجع إلى العميل مساويًا لمبلغ الضريبة المحصل بالأصل.

