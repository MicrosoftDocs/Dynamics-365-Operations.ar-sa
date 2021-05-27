---
title: لا يمكن لمسؤولي النظام مسح قوائم الاحتجاز لأنهم غير مخولين
description: لا يمكن لمسؤولي النظام مسح قوائم الاحتجاز لأنهم غير مخولين.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026252"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="b6c1e-103">لا يمكن لمسؤولي النظام مسح قوائم الاحتجاز لأنهم غير مخولين</span><span class="sxs-lookup"><span data-stu-id="b6c1e-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="b6c1e-104">رقم KB: 4614642</span><span class="sxs-lookup"><span data-stu-id="b6c1e-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="b6c1e-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="b6c1e-105">Symptoms</span></span>

<span data-ttu-id="b6c1e-106">لا يمكن لمسؤولي النظام مسح أمر المبيعات ما لم يكن لديهم الدور المحدد الذي تم تعيينه في كود القائمة الخاص بالأمر.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="b6c1e-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="b6c1e-107">Resolution</span></span>

<span data-ttu-id="b6c1e-108">يتم الوصول إلى بعض العمليات، مثل مسح قوائم الاحتجاز لأوامر المبيعات، من خلال إعداد نهج العمل.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="b6c1e-109">ولا يسمح لمسؤولي النظام عادة بتنفيذ عمليات من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="b6c1e-110">وبشكل أكثر تكرارًا، يتم التحكم في الوصول إلى تنفيذ مهمة معينة بواسطة نهج العمل، ويتم اعتماد أشخاص معينين فقط في مؤسسة ما لتنفيذ تلك المهمة.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="b6c1e-111">وتتضمن الأمثلة الموافقات الناتجة عن اعتمادات سير العمل والمهام المحددة الناتجة عن تكوين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="b6c1e-112">علة الرغم من عدم اقتران أي سير عمل بقوائم الاحتجاز الخاصة بالأمر، فإن القاعدة تكون مشابهة.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="b6c1e-113">ويحدد الدور المرتبط مجموعة معينة من الأشخاص في مؤسسة لها حق مسح قوائم الاحتجاز الخاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="b6c1e-114">يجب ألا يتم منح هذا الحق بالضرورة لكافة المسؤولين، لأن ذلك الأسلوب ينتهك سياسة العمل المحددة.</span><span class="sxs-lookup"><span data-stu-id="b6c1e-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
