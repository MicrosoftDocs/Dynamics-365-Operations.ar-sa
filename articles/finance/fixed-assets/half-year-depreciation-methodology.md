---
title: منهج قاعدة إهلاك نصف السنة
description: يصف هذا الموضوع الأسلوب الذي تستخدمه الأصول الثابتة لحساب الإهلاك باستخدام قاعدة نصف السنة، والذي يحسب سته أشهر من الإهلاك خلال العامين الأول والأخير من وضع الأصل قيد الخدمة.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977229"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="d88ef-103">منهج قاعدة إهلاك نصف السنة</span><span class="sxs-lookup"><span data-stu-id="d88ef-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d88ef-104">يصف هذا الموضوع الأسلوب المستخدم في الأصول الثابتة لحساب الإهلاك باستخدام قاعدة نصف السنة.</span><span class="sxs-lookup"><span data-stu-id="d88ef-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="d88ef-105">تحسب قاعدة نصف السنة سته أشهر من الإهلاك خلال العامين الأول والأخير من وضع الأصل قيد الخدمة.‬</span><span class="sxs-lookup"><span data-stu-id="d88ef-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="d88ef-106">لمزيد من المعلومات حول قواعد الإهلاك، راجع [أساليب وقواعد الإهلاك](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="d88ef-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="d88ef-107">عند استخدام قواعد الإهلاك من سته أشهر، يستخدم النظام سنة الاستحواذ أو سنة وضع الأصل قيد الخدمة، ثم يحسب خمس سنوات من الإهلاك اعتبارًا من ذلك العام، ثم يضيف ستة أشهر.</span><span class="sxs-lookup"><span data-stu-id="d88ef-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="d88ef-108">لتوضيح هذه العملية، يمكنك افتراضي أصل تم الاستحواذ عليه بسعر 50,000، وتم وضعه قيد الخدمة في أبريل 2020.</span><span class="sxs-lookup"><span data-stu-id="d88ef-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="d88ef-109">ويمكنك أن تفترض أيضًا أن عمر الخدمة لهذا الأصل هو خمس سنوات.</span><span class="sxs-lookup"><span data-stu-id="d88ef-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="d88ef-110">سوف تنتهي سنة الخدمة الأولى في ديسمبر 2020 ، مما يعني أن انتهاء خدمة الأصل من خمس سنوات ستكون في ديسمبر 2024.</span><span class="sxs-lookup"><span data-stu-id="d88ef-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="d88ef-111">ستقوم قاعده إهلاك نصف السنة بإضافة ستة أشهر إلى عمر الأصل، مما يعني أن عمر الخدمة سينتهي في يونيو 2025.</span><span class="sxs-lookup"><span data-stu-id="d88ef-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="d88ef-112">الإهلاك السنوي 50,000/5 = 10,000 الإهلاك الشهري 10,000/12 = 833.33</span><span class="sxs-lookup"><span data-stu-id="d88ef-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="d88ef-113">إهلاك السنة الأولى 10,000/2 = 5,000 والإهلاك الشهري التالي 5,000/9 = 555.56</span><span class="sxs-lookup"><span data-stu-id="d88ef-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="d88ef-114">[![جدول الإهلاك لقاعدة إهلاك نصف السنة](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="d88ef-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="d88ef-115">توفر فترات الإهلاك الممتدة التي تضيفها قاعدة النصف سنة توزيعًا أكثر دقة للإهلاك.</span><span class="sxs-lookup"><span data-stu-id="d88ef-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="d88ef-116">تمثل قاعدة الستة أشهر مصروفات الإهلاك بطريقة متساوية، الأمر الذي يعتبر مفيدًا لإعداد تقرير كشف الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="d88ef-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
