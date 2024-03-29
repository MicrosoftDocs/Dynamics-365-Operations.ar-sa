---
title: إعدادات المورّد المضافة للتكلفة المستلمة
description: يصف هذا المقال الحقول الجديدة التي تمت إضافتها إلى صفحة البائعين الموجودة عند تمكين وحدة التكلفة المستلمة. يمكنك استخدام هذه الحقول لإعداد البائعين الذين ستستخدمهم مع ميزات التكلفة المستلمة.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 84d1dee0815b036a3d411eabff49d8a08249bed3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882565"
---
# <a name="vendor-settings-added-for-landed-cost"></a>إعدادات المورّد المضافة للتكلفة المستلمة

[!include [banner](../../includes/banner.md)]

عند تمكين وحدة **التكلفة المستلمة**، تتم إضافة العديد من الحقول الجديدة إلى صفحة **الموردين** الموجودة. يمكنك استخدام هذه الحقول لإعداد البائعين الذين ستستخدمهم مع ميزات التكلفة المستلمة.

لتعيين الحقول المناسبة، انتقل إلى **الشراء والتوريد \> الموردون \> جميع الموردين**. افتح موردًا موجودًا، أو أنشئ موردًا جديدًا، ثم حدد علامة التبويب السريع **التفاصيل المتنوعة**. تظهر كل الحقول الجديدة التي تضيفها وحدة **التكلفة المستلمة** ضمن رأس **الرحلات**. يصف الجدول التالي هذه الحقول.

| الحقل | الوصف |
|---|---|
| نوع الشحن | <p>حدد دور المورد فيما يتعلق بالتكلفة المستلمة:</p><ul><li>**بلا** – لا يتمتع المورد بدور خاص مرتبط بالتكلفة المستلمة. هذه القيمة هي الإعداد الافتراضي، لأنه من المحتمل ألا يكون لمعظم الموردين دور محدد.</li><li>**شركه الشحن** - المورد هو شركه شحن. يتوفر الموردون الذين لديهم نوع الشحن هذا للتحديد في حقل **شركة الشحن** في صفحة **الرحلات**.</li><li>**وسيط الجمارك** – يعد المورد أحد وسطاء الجمارك. يتوفر الموردون الذين لديهم نوع الشحن هذا للتحديد في حقل **وسيط الجمارك** في صفحة **السجلات**.</li><li>**المندوب** – المورد هو مندوب. يتوفر الموردون الذين لديهم نوع الشحن هذا للتحديد في حقل **المندوب** في صفحتي **الموردين** و **أوامر الشراء**.</li></ul> |
| مجموعة أنواع التكاليف | قم بتعيين المورد لمجموعة نوع التكلفة بغرض تحديد [التكاليف التلقائية](auto-cost-setup.md). |
| مرفأ المغادرة | حدد ميناء المنشأ للرحلة. |
| الوكيل | المندوب الافتراضي عندما تتم عمليات الشراء من المورد. |
| مورّد احتساب تكلفة الاستيراد | <p>وضّح ما إذا كان المورّد هو مورّد التكلفة المستلمة.</p><p>**تلميح:** يمكنك استخدام هذا الحقل مع الأمان على مستوى السجل للحد من أوامر الشراء التي تظهر عند إنشاء رحلة.</p> |
| شركة الشحن | حدد شركة الشحن الافتراضية التي يتم استخدامها عند إنشاء أوامر الشراء للمورد. |
| موفر الخدمات | وضّح ما إذا كان المورد هو مقدم خدمات. |
| مجموعة تفاوت الزيادة/النقصان‬ | حدد مجموعة تفاوت الزيادة/النقصان الافتراضية للمورد. |
