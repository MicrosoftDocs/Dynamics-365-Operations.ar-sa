---
title: الحد وحد استثنائي
description: يصف هذا الموضوع الحد والحدود الاستثنائية للضريبة المخصومة في المصدر (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022992"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>الحد وحد استثنائي

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الحد والحدود الاستثنائية للضريبة المخصومة في المصدر (TDS). يتم حساب TDS في الفواتير والمدفوعات دائمًا باعتبار الحد والحد الاستثنائي المحدد لمكونات الضريبة TDS في الصفحة **مكونات ضريبة الخصم**. يتم إرفاق مكونات ضريبة TDS بأكواد ضريبة TDS، والتي يتم تضمينها في مجموعات ضريبة TDS. يتم إرفاق مجموعات ضريبة TDS بالموردين والعملاء لحساب TDS على مستوى الفاتورة أو مستوى الدفع.

يتم حساب TDS إذا كان مبلغ الحركة أو الحركات التراكمية التي تم ترحيلها باستخدام مجموعة TDS محددة لمورد يتجاوز الحد المعين في الصفحة **مكونات ضريبة الخصم**. لن يتم حساب TDS حتى يتجاوز مبلغ الحركة التراكمية الحد المعين.

إذا تم تحديد الحد الاستثنائي بالإضافة إلى الحد لمكون TDS، يتم حساب TDS عندما يتجاوز مبلغ حركة معين الحد الاستثنائي حتى وإن لم يتجاوز مبلغ الحركة التراكمية الحد المعين.

### <a name="example"></a>مثال
يتم إعداد مكون الضريبة يسمى TDS وإرفاقه بمجموعة ضريبة TDS والتي تسمى المقاول. تم تحديد الحد على أنه 50.000 وتم تعريف الحد الاستثنائي على أنها 20.000 لمكون ضريبة TDS. يتم تحديد مقاول مجموعة TDS كمجموعة TDS الافتراضية للمورد 1.

يتم ترحيل فاتورة الشراء 001 لمورد 1 لـ 10000. لم يتم حساب TDS للفاتورة نظرًا لعدم عبور مبلغ الفاتورة للحد أو الحد الاستثنائي. يتم ترحيل فاتورة الشراء 002 لمورد 1 لـ 25.000. لم يتم حساب TDS للفاتورة نظرًا لعدم تجاوز مبلغ الفاتورة للحد الاستثنائي. يتم ترحيل فاتورة الشراء 003 لمورد 1 لـ 20.000. يتم حساب TDS للفاتورة نظرًا لأن مبلغ الفاتورة الإجمالي للفواتير الثلاثة التي يتم إصدارها للمورد قد تجاوز الحد. يتم حساب TDS في كافة الفواتير التي يتم إصدارها للمورد الذي لم يتم حساب TDS عليه في وقت سابق. وبالتالي، يتم حساب TDS على 30.000، وهو مبلغ الفاتورة الإجمالي للفاتورتين 001 و 003.

لا يتم اعتبار الحد والحد الاستثنائي لحساب TDS إذا تم تحديد خانة الاختيار **حد الاطلاع** لأكواد ضريبة TDS في المجموعة TDS التي يتم إرفاقها بالحركة. لن يتم استخدام الحد في أكواد ضريبة TDS في المجموعة TDS التي تحتوي على خانة الاختيار **حد الاطلاع**.

في حالة تحديد خانة الاختيار **حد الاطلاع** لمجموعة TDS محددة لبعض الفواتير، ولكن لم يتم تحديدها للفواتير الأخرى التي تم إنشاؤها لمورد/عميل محدد، فقد يتم وضع حساب TDS بدون الاطلاع على الحد الخاص ببعض الفواتير في الاعتبار المبلغ التراكمي في كافة الفواتير التي لم يتم حساب TDS فيها سابقًا.

على سبيل المثال، الحد هو 25000. يتم إنشاء الفواتير التالية للمورد أ.

- الفاتورة 1 – 2.000 – (لم يتم تحديد خانة الاختيار **حد الاطلاع**): لا يتم حساب TDS.

- الفاتورة 2 – 4.000 – (يتم تحديد خانة الاختيار **حد الاطلاع**): يتم حساب TDS على 4.000.

- الفاتورة 2 – 3.000-(لا يتم تحديد خانة الاختيار **حد الاطلاع**): يتم حساب TDS على أنه مبلغ الفاتورة التراكمي، أي ، 27.000 (20000 + 4000 + 3000) يتجاوز الحد. يتم حساب TDS على المبلغ التراكمي للفواتير التي لم يتم احتساب TDS عليها في وقت سابق، أي، 23.000 (20000 + 3000).