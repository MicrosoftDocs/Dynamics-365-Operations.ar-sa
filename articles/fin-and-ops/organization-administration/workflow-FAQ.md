---
title: الأسئلة المتداولة حول سير العمل
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/01/2019
ms.locfileid: "773193"
---
# <a name="workflow-system"></a>نظام سير العمل

[!include [banner](../includes/banner.md)]

يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>الإخطارات

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>لماذا أتلقى إخطارات متعددة عند رفض عنصر عمل؟
عند رفض عنصر عمل، يتم إكمال هذا العنصر كعنصر مرفوض. ويتم إنشاء عنصر عمل آخر وتعيينه إلى المنشئ. وهذا يعني إرسال إخطار إلى المنشئ يتعلق بعنصر العمل المرفوض وإخطار منفصل إلى المستخدم المعيّن إلى عنصر العمل الجديد "التغيير المطلوب‬". 

يتعلق كل إخطار بعنصر عمل مختلف، ولكن التشابه قد يسبب الإرباك. نحن بصدد البحث عن طرق لتحسين هذا الأمر في إصدار مستقبلي.
