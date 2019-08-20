---
title: النفقات الشخصية على تقرير نفقات
description: يشرح هذا الموضوع الأسلوبين المستخدمين لمعالجة المصروفات الشخصية للعامل في Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794970"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="c6610-103">المصروفات الشخصية على تقرير المصروفات</span><span class="sxs-lookup"><span data-stu-id="c6610-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6610-104">أثناء السفر من أجل العمل، قد يقوم العامل أحيانًا باستخدام بطاقة الائتمان الخاصة بالشركة لسداد مصروفاته الشخصية.</span><span class="sxs-lookup"><span data-stu-id="c6610-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="c6610-105">إذا لم تقم بتحديد آلية لمعالجة المصروفات الشخصية، فقد تتعطل عملية الموافقة على تقارير المصروفات عندما يُرسل العمال تقارير مصروفاتهم المفصلة.</span><span class="sxs-lookup"><span data-stu-id="c6610-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="c6610-106">هناك أسلوبان لمعالجة المصروفات الشخصية للعامل في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c6610-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="c6610-107">**مدفوع بواسطة الموظف** - لا تدفع مؤسستك مصروفاتك الشخصية التي تظهر على الفاتورة الخاصة ببطاقة ائتمان الشركة.</span><span class="sxs-lookup"><span data-stu-id="c6610-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="c6610-108">بدلًا من ذلك، يقوم الموظف بإنشاء تقرير يعرض المصروفات الشخصية جنبًا إلى جنب مع مصروفات الشركة التي تم تحميلها على بطاقة ائتمان الشركة.</span><span class="sxs-lookup"><span data-stu-id="c6610-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="c6610-109">**مدفوع بواسطة الشركة** - تدفع مؤسستك الفاتورة كاملة من خلال بطاقة ائتمان الشركة، ثم تقوم بخصم المصروفات الشخصية من حساب العامل.</span><span class="sxs-lookup"><span data-stu-id="c6610-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="c6610-110">يمكنك تحديد الطريقة التي تستخدمها مؤسستك على صفحة **محددات إدارة المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="c6610-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
